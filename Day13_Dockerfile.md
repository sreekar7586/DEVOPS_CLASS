\# Day 13 - Environment Variables and Port Mapping



\## Passing Environment Variables from Host System



Environment variables can be passed from host to container dynamically.



\## Example 1



Step 1: Set variable on host



export APP\_PORT=8080



Step 2: Run container



docker run -e APP\_PORT nginx env



This passes APP\_PORT value into container.



\## Using .env File (Professional Method)



Create a file named .env



DB\_HOST=localhost

DB\_USER=root

DB\_PASS=secret



Run container:



docker run --env-file .env myapp



This method is clean and widely used in real projects.



\## Example 2 (Interactive + Detached Mode)



docker run -it -d httpd



Explanation:

\-it → interactive mode  

\-d → background execution  

httpd → image name  



This command pulls image (if not present) and starts container.



\## Port Mapping (-p option)



Port mapping allows external access to container applications.



\## Syntax



docker run -p <HOST\_PORT>:<CONTAINER\_PORT> IMAGE



\## Explanation



HOST\_PORT → port on your system  

CONTAINER\_PORT → port inside container  



\## Example 1 (Without Port Mapping)



docker run nginx



Result:

Application runs but NOT accessible in browser.



\## Example 2 (With Port Mapping)



docker run -p 8080:80 nginx



Now open browser:

http://localhost:8080



\## Internal Flow



Browser → Host → Container → Application



\## Important Notes



\- Containers run in isolated network

\- Without -p, services are not accessible

\- -p is required for web applications



\## Summary



\- Environment variables help configure containers

\- .env file is best practice

\- Port mapping allows external access

