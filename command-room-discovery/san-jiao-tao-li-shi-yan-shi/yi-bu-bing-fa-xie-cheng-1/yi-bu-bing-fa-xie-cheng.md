# 异步，并发，协程（旧版本折叠）

## **难点：**

### **协程&服务器心跳**

* 协程 grep

[https://docs.python.org/zh-cn/3/library/asyncio-task.html](https://docs.python.org/zh-cn/3/library/asyncio-task.html)

* 【Python】基于协程的并发WebSocket通信实践

[https://blog.csdn.net/pupilxmk/article/details/106429215](https://blog.csdn.net/pupilxmk/article/details/106429215)

### **并发&锁**

* 分布式锁，三种实现方式，性能对比分析！

[https://cloud.tencent.com/developer/article/1720823](https://cloud.tencent.com/developer/article/1720823)

### **异步asyncio**

* 异步asyncio

[https://docs.python.org/zh-cn/3/library/asyncio.html](https://docs.python.org/zh-cn/3/library/asyncio.html)

* aiohttp

[https://pypi.org/project/aiohttp/](https://pypi.org/project/aiohttp/)

* AIOAMQP

[https://pypi.org/project/aioamqp/](https://pypi.org/project/aioamqp/)

## **【Python系列】4**、**协程与异步并发**

**主要内容：**

* 协程与异步

### 异步IO

　　因为一个IO操作就阻塞了当前线程，导致其他代码无法执行，所以我们必须使用多线程或者多进程来并发执行代码，为多个用户服务。每个用户都会分配一个线程，如果遇到IO导致线程被挂起，其他用户的线程不受影响。

　　多线程和多进程的模型虽然解决了并发问题，但是系统不能无上限地增加线程。由于系统切换线程的开销也很**大**，所以，一旦线程数量过多，CPU的时间就花在线程切换上了，真正运行代码的时间就少了，结果导致性能严重下降。

　　由于我们要解决的问题是CPU高速执行能力和IO设备的龟速严重不匹配，多线程和多进程只是解决这一问题的一种方法。

　　另一种解决IO问题的方法是异步IO。当代码需要执行一个耗时的IO操作时，它只发出IO指令，并不等待IO结果，然后就去执行其他代码了。一段时间后，当IO返回结果时，再通知CPU进行处理。

### 协程

　　协程，又称微线程，纤程。英文名Coroutine。

　　子程序，或者称为函数，在所有语言中都是层级调用，比如A调用B，B在执行过程中又调用了C，C执行完毕返回，B执行完毕返回，最后是A执行完毕。

　　所以子程序调用是通过栈实现的，一个线程就是执行一个子程序。

　　子程序调用总是一个入口，一次返回，调用顺序是明确的。而协程的调用和子程序不同。

　　协程看上去也是子程序，但执行过程中，在子程序内部可中断，然后转而执行别的子程序，在适当的时候再返回来接着执行。

**那和多线程比，协程有何优势？**

　　最**大**的优势就是协程极高的执行效率。因为子程序切换不是线程切换，而是由程序自身控制，因此，没有线程切换的开销，和多线程比，线程数量越多，协程的性能优势就越明显。

　　第二**大**优势就是不需要多线程的锁机制，因为只有一个线程，也不存在同时写变量冲突，在协程中控制共享资源不加锁，只需要判断状态就好了，所以执行效率比多线程高很多。

　　因为协程是一个线程执行，那怎么利用多核CPU呢？最简单的方法是多进程+协程，既充分利用多核，又充分发挥协程的高效率，可获得极高的性能。

### generator

　　Python对协程的支持是通过generator实现的。

　　在generator中，我们不但可以通过for循环来迭代，还可以不断调用next\(\)函数获取由yield语句返回的下一个值。

　　但是Python的yield不但可以返回一个值，它还可以接收调用者发出的参数。

　　传统的生产者-消费者模型是一个线程写消息，一个线程取消息，通过锁机制控制队列和等待，但一不小心就可能死锁。

　　如果改用协程，生产者生产消息后，直接通过yield跳转到消费者开始执行，待消费者执行完毕后，切换回生产者继续生产，效率极高：

```text
def ():
    r = ''
    while True:
        n = yield r
        if not n:
            return
        print('[CONSUMER] Consuming %s...' % n)
        r = '200 OK'

def produce(c):
    c.send(None)
    n = 0
    while n < 5:
        n = n + 1
        print('[PRODUCER] Producing %s...' % n)
        r = c.send(n)
        print('[PRODUCER] Consumer return: %s' % r)
    c.close()

c = consumer()
produce(c)
```

注意到consumer函数是一个generator，把一个consumer传入produce后：

* 首先调用c.send\(None\)启动生成器；
* 然后，一旦生产了东西，通过c.send\(n\)切换到consumer执行；
* consumer通过yield拿到消息，处理，又通过yield把结果传回；
* produce拿到consumer处理的结果，继续生产下一条消息；
* produce决定不生产了，通过c.close\(\)关闭consumer，整个过程结束。 　　 　　整个流程无锁，由一个线程执行，produce和consumer协作完成任务，所以称为“协程”，而非线程的抢占式多任务。

### asyncio

　　asyncio是Python 3.4版本引入的标准库，直接内置了对异步IO的支持。

　　asyncio的编程模型就是一个消息循环。我们从asyncio模块中直接获取一个EventLoop的引用，然后把需要执行的协程扔到EventLoop中执行，就实现了异步IO。

　　用asyncio实现Hello world代码如下：

```text
import asyncio

def hello():
    print("Hello world!")
    
    r = yield from asyncio.sleep(1)
    print("Hello again!")

# 获取EventLoop:
loop = asyncio.get_event_loop()
# 执行coroutine
loop.run_until_complete(hello())
loop.close()
```

@asyncio.coroutine把一个generator标记为coroutine类型，然后，我们就把这个coroutine扔到EventLoop中执行。

　　hello\(\)会首先打印出Hello world!，然后，yield from语法可以让我们方便地调用另一个generator。由于asyncio.sleep\(\)也是一个coroutine，所以线程不会等待asyncio.sleep\(\)，而是直接中断并执行下一个消息循环。当asyncio.sleep\(\)返回时，线程就可以从yield from拿到返回值（此处是None），然后接着执行下一行语句。

　　把asyncio.sleep\(1\)看成是一个耗时1秒的IO操作，在此期间，主线程并未等待，而是去执行EventLoop中其他可以执行的coroutine了，因此可以实现并发执行。

```text
import threading
import asyncio


def hello():
    print('Hello world! (%s)' % threading.currentThread())
    yield from asyncio.sleep(1)
    print('Hello again! (%s)' % threading.currentThread())

loop = asyncio.get_event_loop()
tasks = [hello(), hello()]
loop.run_until_complete(asyncio.wait(tasks))
loop.close()
```

### async/await

　　用asyncio提供的@asyncio.coroutine可以把一个generator标记为coroutine类型，然后在coroutine内部用yield from调用另一个coroutine实现异步操作。

　　为了简化并更好地标识异步IO，从Python 3.5开始引入了新的语法async和await，可以让coroutine的代码更简洁易读。

　　请注意，async和await是针对coroutine的新语法，要使用新的语法，只需要做两步简单的替换：

```text
把@asyncio.coroutine替换为async；
把yield from替换为await。
```

　　让我们对比一下上一节的代码：

```text
def hello():
    print("Hello world!")
    r = yield from asyncio.sleep(1)
    print("Hello again!")
```

　　用新语法重新编写如下：

```text
async def hello():
    print("Hello world!")
    r = await asyncio.sleep(1)
    print("Hello again!")
```

　　剩下的代码保持不变。

### aiohttp

　　asyncio可以实现单线程并发IO操作。如果仅用在客户端，发挥的威力不**大**。如果把asyncio用在服务器端，例如Web服务器，由于HTTP连接就是IO操作，因此可以用单线程+coroutine实现多用户的高并发支持。

　　asyncio实现了TCP、UDP、SSL等协议，aiohttp则是基于asyncio实现的HTTP框架。

　　编写一个HTTP服务器，分别处理以下URL：

```text
/ - 首页返回b'<h1>Index</h1>'；
​
/hello/{name} - 根据URL参数返回文本hello, %s!。
```

　　代码如下：

```text
import asyncio
​
from aiohttp import web
​
async def index(request):
    await asyncio.sleep(0.5)
    return web.Response(body=b'<h1>Index</h1>')
​
async def hello(request):
    await asyncio.sleep(0.5)
    text = '<h1>hello, %s!</h1>' % request.match_info['name']
    return web.Response(body=text.encode('utf-8'))
​
async def init(loop):
    app = web.Application(loop=loop)
    app.router.add_route('GET', '/', index)
    app.router.add_route('GET', '/hello/{name}', hello)
    srv = await loop.create_server(app.make_handler(), '127.0.0.1', 8000)
    print('Server started at http://127.0.0.1:8000...')
    return srv
​
loop = asyncio.get_event_loop()
loop.run_until_complete(init(loop))
loop.run_forever()
```

　　注意aiohttp的初始化函数init\(\)也是一个coroutine，loop.create\_server\(\)则利用asyncio创建TCP服务。

## Python中协程\(coroutine\)和生成器\(generator\)的区别

[https://www.jianshu.com/p/5103c6a63e33](https://www.jianshu.com/p/5103c6a63e33)

