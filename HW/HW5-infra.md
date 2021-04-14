# **CSC 519 DevOps -- Homework 5**
# HW #5 Redis
```
J Troy Hunt
jthunt@ncsu.edu 
April 13, 2021
```


### Conceptual Questions

1. Describe three desirable properties for infrastructure.
 - Scalability --> The ability to increase specific units/instances in response to changing demand.
 - Durability --> Ensure that operations and data remain persistent across partitions.
 - Isolation --> Reduce impact of component behavior on other operations.

2. Describe some benefits and issues related to using Load Balancers.
 - Load balancers are beneficial in that they can regulate the resources going to and from specific instances/ environments.
 - However, in the unlikely event that a Load balancer goes down, a backup will have to be able to take its place, or data loss can occur.

3. What are some reasons for keeping servers in seperate availability zones?
 - Separate availability zones can be useful for a few reasons.
 - 1.	Having separate availability zones ensures that in the event of a cascading error only the instances in the nearby zones are affected. 
 - 2.	This can also be useful to ensure that if a hazardous event (Power Outage, Natural Disaster, etc.) is to occur, functionality can still be restored using instances from different zones.

4. Describe the Circuit Breaker and Bulkhead pattern.
 - Bulkheads isolate components and protect from cascading failures through the enforcement of limits. Named after the bulkheads on a ship to prevent hulls from flooding. Essentially a seal is made to ensure that an error does not cascade into later parts on a instance.
 - Circuit Breaker is a way of recognizing repeated failures in order to bypass the timeouts experienced during errors. For example, if an error is alloted 30 seconds to break, and the current status of a structure insures that it is breaking each time, then a Circuit Breaker will bypass this process to ensure the timeout does not occur.
