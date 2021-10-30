# ADR 004: Deployment Topology


# Status
Proposed

# Rationale
Farmacy Family system is being build using multiple different services (service-based architecture style) using same data store so we need to make sure that its easy and cheap to deploy, maintain, and scale on demand. Using any container technology to help with speed, agility and consistency also brings right rigor and maturity within team as well. Currently, there are several options that we could take into consideration as deployment platforms such: on-premise servers, serverless solutions, container orchestrations such as Kubernetes (on-premise or as PaaS) etc. Finally, we could choose to use virtual servers provided by different cloud providers like AWS, GCP (Google Cloud Plartform) or Azure.

# Decision
We decided to go with K8s (Kubernetes for container orchestration) and using AWS EKS (Elastic Kubernetes Service) for few reasons mentioned below.
- Better Scaling Options
    - We can start with minimum instances and decide to scale out/in (scale horisontally, increasing/decreasing the number of running instances) using HPA (Horizontal POD scalling) concept.
    - Horizontal scaling adheres to our architecture where we can scale individual components of our system according to the component's load
- Availibility
    - We will have 3 AZs (Availibility Zones) to make opur application highly available
- AWS managed Service
    - EKS being AWS managed service makes is easy as from devops perspective as we do not need to worry about handling & maintaining K8s clusters/nodes etc.- It does requires some knowledge of K8s but its an investment we can do at start which pay offs very weell in the longer run.

# Consequences
It does requires some knowledge of Kubernetes but its an investment we can do at start which pay offs very well in the longer run, brings better agility and options that aligns better with evolvable architecyle from service-baed to microservices, if that happens in future.