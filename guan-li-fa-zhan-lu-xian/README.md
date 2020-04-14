---
description: BFM Eco System Architecture Design
---

# 【架构】架构设计

{% hint style="success" %}
BFM Unity 将基于 Hyperledger 的公链项目 Besu，

BFM Unity 将使用伊斯坦布尔拜占庭式容错（IBFT）作为共识算法。
{% endhint %}

![](../.gitbook/assets/u-929135687-1423845009-and-fm-26-and-gp-0.jpg)

{% embed url="https://www.hyperledger.org/projects/besu" %}

{% embed url="https://github.com/ethereum/EIPs/issues/650" %}

## BFM Eco System Architecture Design



BFM Eco System adopts a 3-layer architecture divided into Storage Layer, Core Layer, and Application Layer. The BFM protocol adheres to Google Protobuf, which intrinsically supports multi-language extension.

![](../.gitbook/assets/ping-mu-kuai-zhao-20200325-shang-wu-7.14.14.png)

### 1 Core

There are several modules in the core layer, including smart contracts, account management, and consensus. A stack-based virtual machine is implemented on BFM and an optimized instruction set is used. In order to better support DApp developers, Solidity 4 was chosen as the smart contract language, followed by future support of other advanced languages. In addition, BFM's consensus mechanism is based on Delegated Proof of Stake \(DPoS\) and many innovations were made in order to meet its unique requirements.

### 2 Storage

BFM designed a unique distributed storage protocol consisting of Block Storage and State Storage. The notion of a graph database was introduced into the design of the storage layer to better meet the need for diversified data storage in the real world.

#### 2.1 Blockchain Storage

BFM blockchain storage chooses to use LevelDB, which is developed by Google and proven successful with many companies and projects. It has high performance and supports arbitrary byte arrays as both keys and values, singular get, put and delete, batched put and delete, bi-directional iterators, and simple compression using the very fast Snappy algorithm.

#### 2.2 State Storage

BFM has a KhaosDB in the full-node memory that can store all the newly forked chains generated within a certain period of time and supports witnesses to switch from their own active chain swiftly into a new main chain. It can also protect blockchain storage by making it more stable from being terminating abnormally in an intermediate state.

### 3 Application

Developers can create a diverse range of DApps and customized wallets on BFM. Since BFM enables smart contracts to be deployed and executed, the opportunities of utility applications are unlimited.Solidity official documentation: [https://solidity.readthedocs.io/](https://solidity.readthedocs.io/)

### 4 Protocol

 protocol adheres to Google Protocol Buffers 5 , which is a language-neutral, platform-neutral, and extensible way of serializing structured data for use in communications protocols, data storage, and more.

#### 4.1 Protocol Buffers

Protocol Buffers \(Protobuf\) is a flexible, efficient, automated mechanism for serializing structured data, similar to JSON or XML, but much smaller, faster and simpler.

Protobuf \(.proto\) definitions can be used to generate code for C++, Java, C\#, Python, Ruby, Golang Objective-C, and Verilog HDL languages through the official code generators. Various third-party implementations are also available for many other languages. Protobuf eases development for clients by unifying the API definitions and also optimizing data transfers. Clients can take the API .proto from BFM’s protocol repository and integrate through the automatically-generated code libraries.

As a comparison, Protocol Buffers is 3 to 10 times smaller and 20 to 100 times faster than XML, with less ambiguous syntax. Protobuf generates data access classes that are easier to use programmatically.

#### 4.2 HTTP

BFM Protocol provides a websocket & RESTful HTTP API alternative to the Protobuf API. They share the same interface but the HTTP API can be readily used in javascript clients.

### 5 BFM Virtual Machine \(BFM-VM\)

The BFM-VM is a lightweight, Turing complete virtual machine developed for BFM’s ecosystem. The BFM-VM connects seamlessly with the existing development ecosystem to provide millions of global developers with a custom-built blockchain system that is efficient, convenient, stable, secure, and scalable.

### 6 Decentralized Exchange \(DEX\) & Atomic Swap

Google Protocol Buffers official documentation: [https://developers.google.com/protocol-buffers/](https://developers.google.com/protocol-buffers/)

{% embed url="https://en.bitcoin.it/wiki/Atomic\_swap" %}

{% embed url="https://komodoplatform.com/komodo-and-the-early-pioneers-of-atomic-swaps" %}

{% embed url="https://developers.atomicdex.io/" %}

### 7 Implementation

The BFM blockchain code is implemented in Java and was originally a fork from EthereumJ.  
Bancor Protocol official website: [https://about.bancor.network/protocol/](https://about.bancor.network/protocol/)



