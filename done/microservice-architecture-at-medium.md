# Microservice architeture at Medium
[ref](https://medium.engineering/microservice-architecture-at-medium-9c33805eb74f)

## Principles
**Loose coupling, High cohesion, Single purpose**

## Why?
1. Monolithic stack doesnt fit some of engineering needs
2. Product developments keeps getting slow (high coupling, afraid of big changes, entire app deployed as a whole)
3. Single feature scale. They need to scale the whole app 

---
## Quotes
> A microservice is not a service that has a small number of lines of code or does “micro” tasks [...]. Services could be complex and substantial as long as they meet the above three principles.

> In microservice architecture, only one service should be responsible for a specific type of data. All the other services should either request the data through the API of the responsible service or keep a read-only non-canonical (maybe materialized) copy of the data

> Decouple “Building a Service” and “Running Services”. *Those who build the service should not need to worry about network issues, communication protocol, app deployments, observability, etc. Here it comes the need for a plataform team*
