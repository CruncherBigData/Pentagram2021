# ADR 003: Use Service-Based Architecture Style
Farmacy Family system is an extention of an existing application to provide more engagement & analytics exprience to Farmacy engaged customers. Its still running in a start up mode so its very crucial to not invest lot of time facilitating an archtecture style that requires good tooling for collaboration,  development, release and deployment. Also team size is not big hence the overarching architecture style for the Farmacy Family system should be simple, easy to create, maintain and evolve. Evolvability is the key factor we consider here. In other words, Farmacy Family should adopt an established architecture style that suppors evolution.

# Status
Proposed

# Rationale
Both Microservices architecture and Service Oriented architecture (SOA) are considered service-based architectures, meaning that they are architecture patterns that place a heavy emphasis on services as the primary architecture component used to implement and perform business and nonbusiness functionality.

A service-based architecture modularity is at the center of it encouraging encapsulating portions of your application into self-contained services that can be individually designed, developed, tested, and deployed with little or no dependency on other components or services in the application. They all can share the same datastore or we can split them into few datastores as well.

A service-based architecture provides more delivery speed than a monolith or service-oriented architecture (SOA) by breaking the code apart in the domain-centric way advocated by microservice and DDD proponents.

Its evolvable to microservices later in times hen team gets more maturity and familiarity with different systemn components and learn from their initial round of cycles and user feedback.

# Decision
Use Service-based Architecture with one datastore that brings high cohesiveness, low coupling and better transaction manageability. We ill use following principles to deal ith distributed nature of the system.
- Define & share service contrats
    - As we will have fewer services so will use `service-based contracts` which brings speed & agility
- Use Orchestration rather than Choreography for communication
- Use Circuit brakers to make sure we handle service related operational issues (service not avaiulable for example)

# Consequences
There are well known trade-offs for any distributed architectures and service-baed is of no exception. We called out how we will deal with these in general under the decision section.

- Increased complexity
- Cost
- Service Contracts
- Service Responsiveness & Availbility