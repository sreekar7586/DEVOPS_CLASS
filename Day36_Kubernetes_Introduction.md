\# Day 36 - Introduction to Kubernetes



Kubernetes is a container orchestration platform used to manage containerized applications.



\## What is Kubernetes?



\- Open-source orchestration tool

\- Manages Docker containers

\- Automates deployment and scaling



\## Why Kubernetes?



Docker can manage containers on one system.



Kubernetes manages:

\- Multiple containers

\- Multiple servers

\- Large applications



\## Features



\- Auto scaling

\- Self-healing

\- Load balancing

\- Service discovery

\- Rolling updates



\## Kubernetes Architecture



1\. Master Node

\- Controls cluster

\- Schedules workloads



2\. Worker Node

\- Runs containers



\## Important Components



\### Pod

Smallest deployable unit.



\### Deployment

Manages replicas of pods.



\### Service

Exposes application to network.



\### Namespace

Logical separation of resources.



\## Basic Commands



kubectl get pods



kubectl get services



kubectl create deployment myapp --image=nginx



\## Difference Between Docker and Kubernetes



Docker:

\- Container platform



Kubernetes:

\- Container orchestration platform



\## Real World Usage



\- Google

\- Netflix

\- Amazon

\- Spotify



\## Notes



\- Kubernetes commonly uses Docker containers

\- Used in cloud environments

\- Important DevOps skill



\## Summary



Kubernetes automates deployment, scaling, and management of containerized applications.

