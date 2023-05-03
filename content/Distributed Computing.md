---
title: "Distributed Computing"
date: 2023-05-04
tags: ['cloudcomputing']
---

## Distributed Computing 

> "A distributed system is a collection of independent computers that appears to its users as a single coherent system."


a single task is divided **among multiple computers** that communicate with **each other over a network** 

### Features 
several **autonomous** computational entities called **NODES**
each with their own local memory (no shared memory)
communicate via **message passing** 
scalable  

### Elements  of Distributed 

**user interface client** 
	provides info 
	helps monitor and control the system
	not on the same system as primary controller usually

**primary controller** 
_Main Controller_ 
which acts as a broker of information between the frontends and the solvers

**secondary controller**
	communications controller 
	regulating the flow of server processing requests and managing the system’s translation load
	
**system datastore** 
	shared system datastore, either in one computer or distrubuted among many 
	each computer has local memory 
	
***database*** 
	relational database 
	allows multiple users to access same info simultaneously 
	shared database helps synchronization

### Advantages of Distributed  
- larger storage and memory, faster compute, and higher bandwidth than a single machine
- might be more cost efficient (compared to a single big powerful computer)
- no single point of failure
- redundancy, fault tolerance 
- SCALABLE 

### Types 
1. Mainframe
2. Cluster 
3. Grid 

### Applications 
- email by ARPANET was the largest and most successful implementation of distributed computing 
- Peer-2-Peer (such as Torrents, file sharing)


--- 
<sub>sources: <br>
M. van Steen and A.S. Tanenbaum, Distributed Systems, 4th ed., distributed-systems.net, 2023
</sub>