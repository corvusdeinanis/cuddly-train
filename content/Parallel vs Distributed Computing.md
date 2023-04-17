---
title: "Parallel vs Distributed Computing"
date: 2023-04-16
tags: ['cloud', 'cloudcomputing']
---
#cloud #cloudcomputing 

**AT A GLANCE**

| parallel | distributed |
|---|---|
|single computer|multiple computers|
|many operations simultaneously|system components are located at different locations |
|multiple processors|multiple computers|
|shared or distributed memory | ONLY distributed|
|Processors communicate using bus|computer communicate w each other through message passing|
|improves system performance|improves scalability, fault tolerance, resource sharing|

## Serial Computing / Sequential Computing 
one task(operation/instruction) at a time, in sequence 

```mermaid
flowchart LR
d-->c-->b-->a-->x(processor)
a(task a)
b(task b)
c(task c)
d(task d)
```

## Silly drawing I made to understand parallel computing better

![[images/Pasted image 20230417024946.png]]

## Parallel Computing 
**many instructions** are carried out **simultaneously** 
depending on the theory that large problems can often be divided into smaller ones, and then solved concurrently ("in parallel")

### Why did it arise? 
- due to hitting a bottleneck in terms of frequency scaling [^1]
- higher frequency = more power draw, more heat generated 
- so instead, we have been able to reduce space needed for components and  pack more computational power in. More compute models instead of higher frequency 

### Features 
- main model in computers, as multi-core processors (multiple processing units on the same chip)
- saves time and money 
- improves performance 
- SINGLE COMPUTER
-  can use shared or distributed memory 
- COMMUNICATION between cores VIA BUS 
- Fault Tolerance (if one core fails, other is there; redundancy)


[^1]: Frequency scaling or ramping was the dominant force in  processor performance increases from the mid-1980s until roughly the end of 2004. Frequency Scaling = increasing the frequency of the processor / clock, thereby reducing runtime. 

![[images/parallel computing(2).png]]

A problem is broken down in into smaller parts each of which is processed simultaneously by multiple cores / processors
![[images/parallel computing(1).png]]
(two cores sharing the same shared storage)

### Elements of Parallel Computing 
1. Computational Problem    
	three types: 
	numerical, logical reasoning, transaction processing 
	complex problems might need all 
2. Computer Architecture 
	   Von Neumann architecture to multi-core and  multi-computer
	   lots of revolutionization
3. Performance 
	depends on machine capability and program behaviour 	
4. Application Software 
	   type of computer program that performs specific functions
	   end-user software
5. OS
	   interface between a computer user and computer hardware
	   file management, memory management
	   basic functions
6. Hardware Architecture 
	   Single instruction single data (SISD)
	   Multiple instruction  Single Data (MISD)
	   Single instruction multiple data (SIMD)
	   Multiple instruction multiple data (MIMD)
7. Mapping
	   specfies where to execute each task

## Distributed Computing 

> "A distributed system is a collection of independent computers that  
	appears to its users as a single coherent system."


a single task is divided **among multiple computers** that communicate with **each other over a network** 

### Features 
several **autonomous** computational entities called **NODES**
each with their own local memory (no shared memory)
communicate via **message passing** 
scalable  

### Elements  of Distributed 
(???check most of these just to be a direct paste from IBM documentation for one of their server models??)

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


[[Cloud Computing Unit 1]]

also see - [[Moore's Law]]