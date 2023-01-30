## Diktyo-io project

This project introduces several components for the Kubernetes platform 
to model/weight a cluster's network latency and topological information, 
and leverage that to better schedule latency- and bandwidth-sensitive workloads.

# Introduction

Many applications are latency-sensitive, demanding lower latency between microservices in the application. Scheduling policies that aim to reduce costs or increase resource efficiency are not enough for applications where end-to-end latency becomes a primary objective.

Applications such as the Internet of Things (IoT), multi-tier web services, and video streaming services would benefit the most from network-aware scheduling policies, which consider latency and bandwidth in addition to the default resources (e.g., CPU and memory) used by the scheduler.

Users encounter latency issues frequently when using multi-tier applications. These applications usually include tens to hundreds of microservices with complex interdependencies. 
Distance from servers is usually the primary culprit. 
The best strategy is to reduce the latency between chained microservices in the same application, according to the prior work about Service Function Chaining (SFC).

Besides, bandwidth plays an essential role for those applications with high volumes of data transfers among microservices. For example, multiple replicas in a database application may require frequent copies to ensure data consistency. Spark jobs may have frequent data transfers among map and reduce nodes. Insufficient network capacity in nodes would lead to increasing delay or packet drops, which will degrade the Quality of Service (QoS) for applications.

We propose several network-aware components for the Kubernetes platform 
that focus on delivering low latency to end-users and ensuring bandwidth 
reservations in pod scheduling.

# Contribution guidelines

[CNCF Code of Conduct](https://github.com/cncf/foundation/blob/main/code-of-conduct.md)


