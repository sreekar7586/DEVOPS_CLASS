\# Day 19 - Docker Networking



Docker networking allows containers to communicate with each other and external systems.



\## Default Network



If not specified, Docker uses:

bridge network



\## Types of Networks



1\. Bridge (default)

2\. Host

3\. None

4\. User-defined network

5\. Overlay (advanced)



\## Bridge Network



Default network for containers



docker run nginx



\## User-Defined Network



Create network:



docker network create mynet



Run container:



docker run -d --name app --network mynet nginx

docker run -d --name db --network mynet mysql



\## Benefits



\- Containers can communicate using names

\- Better isolation



\## Host Network



docker run --network host nginx



Container uses host network directly.



\## None Network



docker run --network none ubuntu



No internet, fully isolated.



\## Inspect Network



docker network inspect mynet



\## List Networks



docker network ls



\## Notes



\- Networking is required for microservices

\- Containers communicate using IP or name



\## Summary



Docker networking enables communication between containers and external systems.

