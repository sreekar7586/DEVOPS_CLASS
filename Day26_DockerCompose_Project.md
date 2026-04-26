\# Day 26 - Docker Compose Full Project



This project demonstrates running multiple services using Docker Compose.



\## Objective



Deploy a web server (nginx) and database (MySQL) using a single YAML file.



\## Step 1 - Create docker-compose.yml



version: "3"



services:



&#x20; web:

&#x20;   image: nginx

&#x20;   ports:

&#x20;     - "8080:80"

&#x20;   depends\_on:

&#x20;     - db



&#x20; db:

&#x20;   image: mysql:8

&#x20;   environment:

&#x20;     MYSQL\_ROOT\_PASSWORD: root

&#x20;     MYSQL\_DATABASE: myapp

&#x20;   volumes:

&#x20;     - db\_data:/var/lib/mysql



volumes:

&#x20; db\_data:



\## Step 2 - Start Services



docker compose up -d



\## Step 3 - Check Running Containers



docker compose ps



\## Step 4 - View Logs



docker compose logs

docker compose logs -f



\## Step 5 - Stop Services



docker compose down



\## Advantages



\- Single file deployment

\- Easy to manage multiple containers

\- Used in real-world DevOps



\## Notes



\- YAML indentation is important

\- services define containers

\- volumes store persistent data



\## Summary



Docker Compose simplifies multi-container deployment using a single configuration file.

