# BLOCKCHAIN

The blockchain technology is currently at the _peak of inflated expectations_ and is expected to be ready for mainstream adoption in 5 to 10 years.

Various benefits of this technology are being envisaged such as decentralized trust, cost savings, transparency, and efficiency.
To understand the blockchain technology we have to focus on the distributed systems first because it is his roots.

##Distributed systems

Distributed systems are a computing paradigm whereby two or more nodes work with each other in a coordinated fashion in order to achieve a common outcome and it's modeled in sucha a way that end users see it as a single logical platform.

A *node* can be defined as an individual player in a distributed system. All nodes are capable of sending and receiving messages to and from each other. Nodes can be honest, faulty, or malicious and have their own memory and processor. A node that can exhibit arbitrary behavior is also know as a _Byzantine node_. This arbitrary behavior can be intentionally malicious, which is detrimental to the operation of the network. Generally, *any unexpected behavior of a node on the network can be categorized as Byzantine*. This term arbitrarily encompasses any behavior that is unexpected or malicious.

Distributed systems are so challenging to design that a theorem known as the CAP theorem has been proved and states that a distributed system cannot have all much desired properties simultaneously.

CAP THEOREM

This is also known as Brewer's theorem. The theorem states that any distributed system cannot have Consistency, Availability, and Partion tolerance simultaneously:

   **Consistency** is a property that ensures that all nodes in a distributed system have a single latest copy of data.
    
   **Availability** means that eh system is up, accesible for use, and is accepting incoming requests and responding with data without any failures as and when required.
    
   **Partion tolerance** ensures that if a group of nodes fails the distributed system still continues to operate correctly.
    
  It has been proven that a distributed system cannot have all the afore mentioned three properties at the same time.
    
  
 In order to achieve fault tolerance, replication is used. This is a common and widely used method to achieve fault tolerance. Consistency is a achieved using consensus algorithms to ensure that all nodes have the same copy of data. This is also called *state machine replication*. Blockchain is basically a method to achieve state machine replication.
 
 In general, there are two types of fault that a node can experience: where a faulty node has simply crashed and where the faulty node can exhibit malicious or inconsistent behavior arbitrarily. This is the type which is difficult to deal with since it can cause confusion due to misleading information.
 
 BYZANTINE GENERAL PROBLEM
 
 We've seen that Byzantine nodes are nodes which have an arbitrary behavior. In order to resolve the problem, a consensus was created. The consensus is a process of agreement between distrusting nodes on a final state of data. In order to achieve consensus different algorithms can be used. It easy to reach an agreement between two nodes but when multiple nodes are participating in a distributed system and they need to agree on a single value it becomes very difficult to achieve consensus. This concept of achieving consensus between multiple nodes is known as distributed consensus.
 
 
 CONSENSUS MECHANISMS.
 
 A consensus mechanisms is a set of steps that are taken by all, or most, nodes in order to agree on a proposed state of value. For more than three decades this concept has been researched by computer scientists in the industry and Academia. Consensus mechanisms have recently come into the limelight and gained much popularity with the advent of bitcoin and blockchain.

There are various requirements which must be met in order to provide the desired results in a consensus mechanism:

  Agreement: All honest nodes decide on the same value
  
  Termination: All honest nodes terminate execution of the consensus process and eventually reach a decision
  
  Validity: The value agreed upon by all honest nodes must be the same as the initial value proposed by at least one honest node.
  
  Fault tolerant: The consensus algorithm should be able to run in the presence of faulty or malicious nodes.
  
  Integrity: This is a requirement where by no node makes the decision more than once. The nodes make decisions only once in a single consensus cyrcle.
  
TYPES OF CONSENSUS MECHANISM.

  *Byzantine fault tolerance-based*: With no compute intensive operations such as partial hash inversion, this method relies on a simple scheme of nodes that are publishing signed messages. Eventually, when a certain number of messages are received, then an agreement is reached.
 
 *Leader-based consensus mechanisms*: This type of mechanisms requires nodes to complete for the _leader-election lottery_ and the node that wins it proposes a final value.
 
Paxos is the most famous protocol which have been proposed. In Paxos nodes are assigned various roles such as Proposer, Acceptor, and Learner. Nodes or processes are named replicas and consensus is achieved in the presence of faulty nodes by agreement among a majority of nodes.

RAFT, and alternative to Paxos, works by assigning any of three states, that is, Follower, Candidate, or Leader, to the nodes. A Leader is elected after a candidate node receives enough votes and all changes now have to go through the Leader, who commits the proposed changes once replication on the majority of follower nodes is completed.

THE CONCEPT OF ELECTRONIC CASH.

 This concept is also essential to appreciate the first and astonishingly successful application of blockchain.
 
 Fundamental issues that need to be addressed in e-cash systems are accountability and anonymity. _David Chaum_ addressed both of these issues by introducing two cryptographic operations, namely blind signatures and secret sharing:
 
  *Blind signatures* allow signing a document without actually seeing it.
  
  *Secret sharing* is a concept that allows the detection of using the same e-cash token twice.
 
A different but relevant concept called *hashcash* was introduced by _Adam Back_ in 1997 as a PoW system to control e-mail spam. The idea of Hashcash is simple: if a legitime users want to send e-mails then they are required to compute a hash as a proof that they have spent a reasonable amount of computing resources before sending the e-mail.

In 2009 the first practical implementation of cryptocurrency named *bitcoin* was introduced; for the very first time it solved the problem of distributed consensus in a trustless network. It uses public key cryptography with hashcash as PoW to provide a secure, controlled and decentralized method of minting digital currency.


## INTRODUCTION TO BLOCKCHAIN.

Blockchain is a peer-to-peer distributed ledger that is cryptographically secure, append-only-m, immutable, and updateable only via consensus or agreement among peers.

Blockchain can be though of as a layer of distributed peer-to-peer network running on top of the Internet.

*From a business point of view* a blockchain can be defined as a platform whereby peers can exchange values using transactions wihout the need for a central trusted arbitrator. This is a poweful concept and once readers understand it they will realize the tsunamic potential of blockchain technology. This allows blockchain to be decentralized consensus mechanism where no single authority is in charge of the database.

A block is simply a selection of transactions bundled together in order to organize them logically. It is made up of transactions and its size is variable depending on the type and design of the blockchain in use. A reference to a previous block is also incluided in the block unless it's a genesis block. A genesis block is the first block in the blockchain that was hardcoded at the time the blockchain was started. The structure of a block is also dependent on the type and design of a blockchain, but generally there are a few attributes that are essential to the functionality of a block, such as the block header, pointers to previous blocks, the time stamp, nonce, transaction counter, transactions, and other attributes.

### TECHNICAL DEFINITIONS OF BLOCKCHAIN.  

  Blockchain is a decentralized consensus mechanism. In a blockchain, all peers eventually come to an agreement regarding the state of a transaction.
  Blockchain is a distributed shared ledger. Blockchain can be considered a shared ledger of transactions. The transactions are ordered and grouped into blocks. Currently, the real-world model is based on private databases that each organization maintains whereas the distributed ledger can serve as a single source of truth for all member organizations that are using blockchain.
  Blockchain is a data structurer; it is basically a linked list that uses hash pointers instead of normal pointers. Hash pointers are used to point to the previous block.
  
## GENERIC ELEMENTS OF A BLOCKCHAIN.

1. Addresses.

Addresses are unique identifiers that are used in a transaction on the blockchain to denote senders and recipients. An address is usually a public key or derived from a public key. While Addresses can be reused by the same user, addresses themselves are unique. In practice, however, a single user may not use the same address again and generate a new one for each transaction. Bitcoin is in fact a pseudonymous system. End users are usually not directly identificable but some research in de-anonymizing bitcoin users have shown that all users can be identified successfully. As a good practice it is suggested that users generate a new address for each transaction in order to avoid linking transactions to the common owner, thus avoiding identification.

2. Transaction.

A transaction is the fundamental unit of a blockchain. A transaction represents a transafer of value from one address to another.

3. Block

A block is composed of multiple transactions and some other elements such as the previous block hash, timestap and nonce.

4. Peer-to-peer network.

As the name implies, this is a network topology whereby all peers can communicate with each other and send and receive messages.

5. Scripting or programming language.

This element performs various operations on a transaction. Transactions scripts are predefined sets of commands for nodes to transfer tokens from one address to another and perform various other functions. Turing complete programming language is a desirable feature of blockchains; however, the security of such languages is a key question and an area of important and ongoing research.

6. Virtual machine.

This is an extension of a transaction script. A virtual machine allows Turing complete code to be run on a blockchain whereas a transaction script can be limited in its operation. Virtual machines are not available on all blockchains; however, various blockchains use virtual machines to run programs.

7. State machine.

A blockchain can be viewed as a state transition mechanism whereby a state is modified form its initial form to the next and eventually to a final form as a result of a transaction execution and validation process by nodes.

8. Nodes.

A node in a blockchain network performs various functions depending on the role it takes. A node can propose and validate transactions and perform minting to facilitate consensus and secure the blockchain. This is done by following a consensus protocol. Nodes can also perform other functions such as simple payment verification, validators, and many others functions depending on the type of the blockchain used and the role assigned to the node.

9. Smart contracts.

These programs 
