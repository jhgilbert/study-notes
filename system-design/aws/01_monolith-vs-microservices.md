# Monolith vs. microservices

## Monoliths overview

A monolith is a single-tiered software application in which the user interface and data access code are combined into a **single program** from a **single platform**.

Monoliths are well-suited for a small user base, in terms of cost, engineering complexity, etc.

At a larger scale, monoliths are less ideal:

- The code may not be very modular, can feel like spaghetti code
- The code cannot be partially deployed

## Monolith APIs vs microservice APIs

### Monolith API

You can have an API without using microservices. Any web requests, such as a request to "users/get", would go through an API Gateway/load balancer that sends the request to one of your monolith instances. These monolith instances can all share a database.

This architecture isn't very scalable:

Each monolith instance is running on its own VM (such as EC2). If the CPU usage spikes for a given request, autoscaling will create a whole new VM, even if the application typically doesn't use very much of the CPU.

### Microservice API

Imagine instead that each endpoint (such as "users/get") has its own microservice running on its own instance. A smaller instance could be used for each endpoint, and different instance sizes can be used depending on how much resources a given endpoint typically needs.

In real-world scenarios, these microservices might still share a database, even if that's not pure microservice architecture.

Another advantage is that each service can be written in a different language and maintained by a different team.

## Characteristics of microservice architectures

Microservices are independent of each other. This yields flexibility around many facets: deployment, security configurations, testing, etc.
