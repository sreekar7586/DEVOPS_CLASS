\# Day 35 - Docker Swarm and Clustering



Docker Swarm is Docker’s native container orchestration tool.



\## What is Docker Swarm?



Docker Swarm allows managing multiple Docker nodes as a cluster.



It helps in:

\- Scaling containers

\- High availability

\- Load balancing



\## Types of Nodes



1\. Manager Node

\- Controls the swarm

\- Schedules services



2\. Worker Node

\- Runs containers



\## Initialize Swarm



docker swarm init



This command initializes Docker Swarm.



\## Check Swarm Status



docker info



Look for:

Swarm: active



\## Join Worker Node



docker swarm join --token <token> <manager-ip>:2377



\## Create a Service



docker service create --name web nginx



\## List Services



docker service ls



\## Inspect Service



docker service inspect web



\## Scale Service



docker service scale web=3



This creates 3 replicas.



\## Remove Service



docker service rm web



\## Leave Swarm



docker swarm leave



\## Advantages



\- Automatic load balancing

\- High availability

\- Easy scaling

\- Cluster management



\## Notes



\- Swarm is useful for large applications

\- Multiple nodes work together

\- Similar concept to Kubernetes



\## Summary



Docker Swarm helps manage containers across multiple systems efficiently.

