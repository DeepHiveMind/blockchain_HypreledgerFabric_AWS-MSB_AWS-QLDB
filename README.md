# Blockchain Hyperledger-Fabric AWS-QLDB AWS-MSB
 
This repo primarily intends to offer  
- Blcokchain Quick Overview 
- Canvassing of 3 major framework/services for Blcokchain
	- **Hyperledger-Fabric** 
	- **AWS-QLDB (AWS Quantum Ledger Database)**
	- **AWS-MSB (AWS Managed Blockchain)**
- Real world application of one of above Blockhain service 
	- Digital Asset Management



* For the ease of addressing, hereon, I'll use following pairs of terms interchangably - 
 - Hyperledger-Fabric as **HLF**
 - Hyperledger as **HL**
 - AWS-QLDB as **QLDB**
 - AWS MSB as **MSB**
 
***
This repo primarily intends to offer distillation of my experience in 3 major Blcokchain frameworks - HLF, QLDB & MSB. 
Please note: 
 - There are very many other popular Blockchain frameworks and tools available in the market in addition to the chosen ones in this repo, such as 
		- 
 
 - Many of these aforemention Blcokchain framework/services are very popular, and are being extensively used.
 - This repo doesn't intend to draw any sort of comparative view between the chosen framework/services and other popular frameworks.
 - This is truly illustrative in nature. 

***

A quick Rundown
- [Blcokchain Quick Overview](#Blcokchain-Quick-Overview)
	
	- [A Sneak Peek into widely used Blockchain frameworks](#A-Sneak-Peek-into-widely-used-Blockchain-frameworks)
	- [When to use Which Framework](#When-to-use-Which-Framework)

- [1 Hyperledger Fabric HLF](#1-Hyperledger-Fabric-HLF)
- [2 AWS Quantum Ledger Database QLDB](#2-AWS-Quantum-Ledger-Database-QLDB)
- [3 AWS Managed Blcokchain AMB](#3-AWS-Managed-Blcokchain-AMB)


# Blcokchain Quick Overview 

### A Sneak Peek into widely used Blockchain frameworks

Sneak Peek into various commonly known Blockchain frameworks 
- **DAPP**: Blcokchain is a DAPPs (Decentralized Applications). 
- ** Data Provenance**: Blcokchain comes baked in with *Data Provenance* by offering *immutable and cryptographically verifiable record of transactions* 
- **"Blcokchain" vis-a-vis "Today’s Systems of Record"**: Please refer to the link to know what difeference Blcokchain brings vis-a-vis *Today’s Systems of Record*.

- Blcokchain Frameworks do vary based on distinct needs, i.e., please choose the right framework from very many Blockchain framework options based on whether you need 
	- a Centralized ledger database,
	- or a Multi-party, 
	- or a Fully managed blockchain network that helps eliminate intermediaries.
- However, The commonality amongst All of the types of available frameworks
	- each offers an *immutable and cryptographically verifiable record of transactions* 
	- each one is also available in *DOCKER (containers)*
	- One can use *Kubernetes (CaaS)* to seamlessly manage and govern these Blockchain containerized workload with the High availability, Auto Scalability, Self healing NFRs. 

- "Today’s Systems of Record" (Distributed Database/ Ledger) vis-a-vis "Blcokchain" (The Future network of Distributed & Decentralized Database/Ledger):
	from the Financial institutions prism POV - 

|"Today’s Systems of Record" (Distributed Database or Ledger) | "Blcokchain" (The Future network of Distributed and Decentralized Database or Ledger)|
| :--: | :--: |
|<img src="/img/current_fin_network_SOR.png" width="300" Height="250" />|<img src="/img/future_net_BLOCHAIN.png" width="300" Height="250" />|
|Click on above image for full view|Click on above image for full view|
|**private programs** & **private Ledger** for Every participant | **shared programs** and **shared ledgers** for Every participant|

*Traditional SOR has all the members of a **business network** transact with each other, but they maintain **separate records of their transactions**. *

### Blcokchain Frameworks Overview

Just a sneak peek into Blcokchain Frameworks through Infographics:

|Blcokchain Framework Conceptual difference | Broader View of Blcokchain Framework|  Commonly used Blcokchain Framework|
| :--: | :--: | :--: |
|<img src="/img/conceptualBC.png" width="300" Height="250" />|<img src="/img/broaderBC.png" width="300" Height="250" />|<img src="/img/commonBC.png" width="300" Height="250" />|
|Click on above image for full view|Click on above image for full view|Click on above image for full view|

### When to use Which Framework

Q. A Specific Question, per say : *"When to use Hyperledger Fabric & When to use Etherum?"*

A. Hyperledger Fabric is well-suited for applications that require *stringent privacy and permission controls with a known set of members*.
     - for example, a ```financial application``` where certain ```trade-related data is only shared with select banks``` .
	 - Ethereum can also be used for joining a public Ethereum blockchain network.
	 
   Whereas, Ethereum is well-suited for highly distributed blockchain networks where transparency of data for all members is important, 
	 - for example, a ```customer loyalty``` blockchain network that allows ```any retailer in the network to independently verify a user's activity across all members to redeem benefits```. 

# 1 Hyperledger Fabric HLF
- The Linux Foundation founded the Hyperledger project in Y2015 to advance cross-industry blockchain technologies. 
- HLF is one of the Framework from *"HL Framework & Tools ecosystem"* with the primary objective to provide **Permissioned with Channel Support**. i.e., HLF is one of the blockchain projects within Hyperledger.

- Like other blockchain technologies (Etherum), it also has 
		- a ledger, 
		- uses smart contracts, 
		- participants manage their transactions,
		- Data Provenance* by offering *immutable and cryptographically verifiable record of transactions* 
		
- Unlike other Blockchain technologies (Ethereum), it differs as
		- private and permissioned,
		- No open permissionless system,
		- No unpermissioned entry to any member/*unknown identities* to participate in the network,
		- No PoW ( “proof of work” protocol to validate transactions and secure the network),
		- Membership Service Provider (MSP):  Restricted Entry to Members of a Hyperledger Fabric network enroll through a trusted MSP

Here is the 'Vantage view of Hyperledger Framework & Tools' - 

Broader ecosystem of *HL Framework & Tools:*

<img src="/img/HLBroaderView.png" width="800" Height="300" />

[Source](https://www.hyperledger.org/wp-content/uploads/2018/07/HL_Whitepaper_IntroductiontoHyperledger.pdf)

### Key Concpets of HLF

- Blockchain network:
	A blockchain network is a technical infrastructure that provides ledger and smart contract (chaincode) services to applications

- Block & Chain: 
	A block contains an ordered set of transactions. It is cryptographically linked to the preceding block, and in turn it is linked to be subsequent blocks.

	The ledger’s chain is a transaction log structured as hash-linked blocks of transactions. Suuch as, Blockchain B contains blocks 0, 1, 2.
	
- Smart Contract:

	A smart contract is code (invoked by a client application external to the blockchain network) that manages access and modifications to a set of *key-value pairs* in the *World State* via Transaction.

	
- Chain Code:

	In Hyperledger Fabric, smart contracts are packaged as chaincode. Chaincode is installed on peers and then defined and used on one or more channels.

- World State:

	*World state* maintains  “current state” of transaction in Ledger, and such data is stored in a state database for efficient reads and queries from chaincode. Supported databases include - *couchDB*.
	
- Channel:
	
	A channel is a private blockchain *overlay* which allows for data isolation and confidentiality. A channel-specific ledger is shared across the peers in the channel, and transacting parties must be authenticated to a channel in order to interact with it. Channels are defined by a *Configuration-Block*.
	
- Membership Service Provider:

	MSP refers to an abstract component of the system that provides credentials to clients, and peers for them to participate in HLF.

- Ordering Service:

	Also known as orderer. A defined collective of nodes that orders transactions into a block and then distributes blocks to connected peers for validation and commit. The ordering service exists independent of the peer processes and orders transactions on a first-come-first-serve basis for all channels on the network.


***
HLF also leverages *Gossip Protocol* & *Raft Algo* for following 3 major functions:
	- 1) manages peer discovery and channel membership; 
	- 2) disseminates ledger data across all peers on the channel; 
	- 3) syncs ledger state across all peers on the channel

The same *protocol* and *Algo* is used in **Progrium Consul** (a distributed computing CONSENSUS Algo for Leader election and worker management), and it is applied in Seneca (a Microservice Framework on Nodejs)
***



### Use Cases of HLF


# 2 AWS Quantum Ledger Database QLDB

### Key Concpets of QLDB


# 3 AWS Managed Blcokchain AMB

### Key Concpets of AMB

# Reference
[1]

[2]https://github.com/senlinuc/caffe_ocr
