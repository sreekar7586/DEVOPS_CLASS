\# Day 14 - Port Mapping and Practical Examples



Port mapping allows external users to access applications running inside containers.



\## Syntax of -p



docker run -p <HOST\_PORT>:<CONTAINER\_PORT> IMAGE



\## Explanation



HOST\_PORT → Port on your system (Laptop/Server)  

CONTAINER\_PORT → Port where application runs inside container  



\## Example 1 (Without Port Mapping)



docker run nginx



Result:

\- Container runs

\- Application is NOT accessible in browser



\## Example 2 (With Port Mapping)



docker run -p 8080:80 nginx



Now open browser:

http://localhost:8080



\## Internal Working



Browser → localhost:8080 → Docker Host → Container:80 → Nginx



\## Example 3 (MySQL Container with Port Mapping)



docker run -d -p 3307:3306 --name mysql-test -e MYSQL\_ROOT\_PASSWORD=root123 mysql



\## Explanation



\-d → Run in background  

\-p 3307:3306 → Map host port 3307 to container port 3306  

\--name → Container name  

\-e → Set environment variable  



\## Access MySQL Container



docker exec -it mysql-test bash



\## Connect to MySQL



mysql -h 127.0.0.1 -P 3306 -u root -p



\## Important Notes



\- Without -p, services are isolated inside container

\- Port mapping is required for web and database access

\- Always match correct ports



\## Summary



\- -p is used to expose container services

\- It connects host and container ports

\- Essential for real-world applications

