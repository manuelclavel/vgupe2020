# Day 2
## Review Day 1
* Module
  - Project
  - Teamwork

* Project
  - A mobile app (for Android <del>and iOS</del>) for booking 
online badminton courts

* Requirements
  - Homework #1

* Architecture
  * 3-tier architecture:
    - modules: presentation, logic, data.</li>
    - advantages: modularity (through well-defined interfaces), 
adaptability to change

* Technology
  - Presentation: <del>Swift (iOS)</del>, Kotlin (Android)
  - Logic: Java
  - Data: MySQL

## Discussion:  Homework #1

## Interfaces
- From Module's Handbook description:
> Students are able to implement a realistic application
> covering aspects of distributed systems and a RDBMS.

### Client-server model
- From Wikipedia:
 
> Client–server model is a __distributed__ application structure 
> that partitions tasks or workloads between 
> the __providers__ of a __resource__ 
> or __service__, called __servers__, and service __requesters__, 
> called __clients__.

> Often clients and servers communicate over a computer network 
> on separate hardware, but both client and server may reside 
> in the same system. 

> A __server__ host runs one or more server programs, 
> which __share__ their resources with clients. 

> A __client__ __does not share__ any of its resources, 
> but it __requests__ content or service from a server. 

> __Clients__ therefore __initiate communication__ sessions with servers, 
> which await incoming requests. 

> Examples of computer applications 
> that use the client–server model are Email, 
> network printing, and the World Wide Web. 

* Related topics
  * Front and back ends
  * Modular programming
  * Observer pattern [Software Engineering Design]
  * Publish–subscribe pattern [Software Engineering Design]
  * Pull technology 
  * Push technology
  * Remote procedure call 

### Stateless protocol
- From Wikipedia

> In computing, a __stateless protocol__ is a communications protocol 
> in which __no session information is retained by the receiver__, 
> usually a server. 

> Relevant session data is sent to the receiver by the client in such a 
> way that every packet of information transferred can be __understood__ 
> in isolation, __without context information__ from previous packets 
> in the session. 

> This property of stateless protocols makes them ideal in high volume 
> applications, increasing performance by removing server load caused 
> by retention of session information.

(...) 

> Examples of stateless protocols include the Internet Protocol (IP), 
> which is the foundation for the Internet, and 
> the Hypertext Transfer Protocol (HTTP), which is the foundation of 
> data communication for the World Wide Web.

> The stateless design __simplifies the server design__ because 
> there is no need to dynamically allocate storage to deal 
> with conversations in progress. 
> If a client session dies in mid-transaction, no part of the system
> needs to be responsible for cleaning up the present state of the
> server.

> A __disadvantage__ of statelessness is that it may be necessary 
> to __include additional information in every request__, 
> and this extra information will need to be interpreted by the server. 


## Homework
- [ ] Design/describe interfaces [client-server] Presentation-Logic
- [ ] Design/describe interfaces [client-server] Logic-Data 
- [ ] Design database (Entity-Relationship Diagram)
- [ ] Design UI (Activity diagram + mockups)




