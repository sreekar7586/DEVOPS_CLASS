\# Day 25 - Docker Mini Project (Nginx + MySQL)



This project demonstrates a multi-container setup using Docker.



\## Objective



Deploy a web server and database using Docker containers.



\## Step 1 - Create Network



docker network create app\_net



\## Step 2 - Create Volume



docker volume create mysql\_data



\## Step 3 - Run MySQL Container



docker run -d \\

\--name mysql\_db \\

\--network app\_net \\

\-e MYSQL\_ROOT\_PASSWORD=root \\

\-e MYSQL\_DATABASE=myapp \\

\-v mysql\_data:/var/lib/mysql \\

mysql:8



\## Step 4 - Run Nginx Container



docker run -d \\

\--name web\_server \\

\--network app\_net \\

\-p 8080:80 \\

nginx



\## Step 5 - Verify Containers



docker ps



\## Step 6 - Check Network



docker network inspect app\_net



\## Step 7 - Test Connectivity



docker exec -it web\_server ping mysql\_db



\## Step 8 - Logs



docker logs web\_server

docker logs mysql\_db



\## Step 9 - Stop Containers



docker stop web\_server

docker stop mysql\_db



\## Step 10 - Remove Containers



docker rm web\_server

docker rm mysql\_db



\## Step 11 - Cleanup



docker volume rm mysql\_data

docker network rm app\_net



\## Notes



\- Containers communicate using network

\- Volume stores database data

\- Multi-container setup is real-world scenario



\## Summary



This project shows how to use Docker networking, volumes, and multiple containers together.

