# systemdesign
 Skeleton : 
1. Gather Requirements and Back of envelope Calculations
    - Functional requirements. 
    - Non functional requirements 
        - Scalability 
        - Availability 
        - Latency and performance 
    - Back of envelope Estimation:
        - number of daily active users 
        - Throughput : 
                calculate Reads and writes per day;  
                Read to write ratio 
        - CAP Tradeoff : 
            - Are we priortitizing Availability, what should be the availability 
            - % availability we're looking at.  
        - Discuss Storage Capacities for the use case. 

Define out of scope functionalities. 

2. API Design and Database Design 
        - API : READ AND WRITE 
                GET /v1/service1 
                       Query Params : {
                                   UserId, 
                                   Timestamp,
                                   title 
                                       }

        - Define Main entities in the problem and relationship between these entities. 
        - Data Base choice : Are we using a Relational db or a Non relational db based on CAP Priorities 
            - Relational Data base 
                - when there are multiple structured tables / data we need to store
                - when there is joins required between the data for this use case. 
                - example : SQL, Postgresql 

            - Non Relational DB. 
                - example: CassandraDb, NoSQL, DynamoDb, MongoDb 

2. High Level Design
   - Common Components:
                - Client/ User 
                - CDN 
                - Load balancer 
                - API Gateway 
                - Microservices 
                - Data base and Cache 
   - Uncommon Components: 
                - Message queues : to handle inflow of requests 
                - rate limiter
                - Authentication and Authorization (OAuth2/ JWT/ role based access control) 
                - Telemetry and Observability : Prometheus, Grafana. 
  
3. Deep Dives.
        Scaling: 
- Scaling Read performance : Discuss Cache (Redis) 
- Scaling Write performance : Discuss Message queues 
- Scaling Database : Discuss Implementing Replicas of data base (also for fault tolerance); Rate limiters and circuit breakers 

    Discuss any tradeoffs (CAP) 


<img width="3756" height="4410" alt="image" src="https://github.com/user-attachments/assets/7e7b27ba-e4a4-41b0-973c-78b0b5375a82" />

# List : 
# 1. Design Top K heavy hitters - HARD
# 2. Design Leet Code - MEDIUM 
# 3. Design Twitter - MEDIUM
