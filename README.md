# SystemDesign
Study material for SystemDesign interviews
We can use following template to solve System design usecases.

Gather Functional Requirements:
  Obtain a detailed problem statement.
  Describe the user's perspective in simple terms.
  Ask clarifying questions to gain a comprehensive understanding.
  
Technical Requirements:
  Determine the user base size.
  Assess the frequency of user interactions (reads/writes).
  Evaluate the size of objects transferred into and out of the system.
  Determine the average size of an object.
  Identify the geographical distribution of users.
  Decide whether the system prioritizes consistency or availability.
  
Designing Microservices:
  Cluster requirements into functional groups, each handled by a separate microservice.
  Distinguish between APIs and data models; segregate them into different microservices if they differ.
  Group user stories around the business objects they manipulate, with each business object becoming a service and its functionalities becoming endpoints.
  
Design Logical Architecture:
  Create one block for each microservice, illustrating the logical flow.
  Utilize REST/HTTP APIs for immediate client response and Message Queues for asynchronous communication.
  Employ Batch Jobs for offline data transfer.
  
Deep Dive into Microservices:
  Each microservice consists of three tiers: Backend tier (business logic), Cache tier (for faster response), and Storage tier (data storage and retrieval).
  DatModel : Schema, selection of cache, selection of storage, estimation 
   How to store in Cache tier
   How to store in Storage tier
   APIs
   Algorithms in APIS
   Flow of API
   Design considerations: CAP theorem,Sharding, API parallelization , LoadBalancers, Datapurge
   Need to scale for Storage?
   Need to scale for throughput?
   Need to scale for Parellelization?  

Identify the Need for Scale:
  Assess scalability requirements for each microservice, considering storage, throughput, API parallelization, hotspots, availability, and geo-distribution.
  Draw a distributed architecture per tier, with strategies like round-robin for stateless app server tiers and shard partitioning for storage tiers.
  Propose algorithms for shard placement, explain API functioning within shard partitions, and suggest replication and consistency/availability strategies.
  Utilize user caches based on problem-specific needs.

we can also read following template for system design problems
  https://www.kcoleman.me/2020/06/14/system-design-interview-format.html

GitHub Repos
https://github.com/systemdesign42/system-design?tab=readme-ov-file
