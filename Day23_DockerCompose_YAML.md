\# Day 23 - Docker Compose YAML File



Docker Compose uses a YAML file to define multi-container applications.



\## What is docker-compose.yml?



It is a configuration file to define services, networks, and volumes.



\## Basic Structure



version: "3"



services:

&#x20; web:

&#x20;   image: nginx

&#x20;   ports:

&#x20;     - "8080:80"



\## Explanation



version → Compose version  

services → List of containers  

web → service name  

image → container image  

ports → port mapping  



\## Multi-Container Example



version: "3"



services:

&#x20; app:

&#x20;   image: nginx

&#x20;   ports:

&#x20;     - "8080:80"



&#x20; db:

&#x20;   image: mysql

&#x20;   environment:

&#x20;     MYSQL\_ROOT\_PASSWORD: root



\## Commands



docker compose up



docker compose up -d



docker compose down



\## Benefits



\- Manage multiple containers easily

\- Single command deployment

\- Better for microservices



\## Notes



\- YAML is indentation sensitive

\- Spaces matter (not tabs)



\## Summary



Docker Compose YAML simplifies multi-container application setup.

