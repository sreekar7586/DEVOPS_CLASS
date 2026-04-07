\# Day 15 - Advanced Environment Variables in Docker



Environment variables allow dynamic configuration of containers.



\## Multiple Environment Variables



docker run -e APP\_ENV=production -e APP\_VERSION=1.0 nginx



This sets multiple variables inside container.



\## MySQL Container Example



docker run -d \\

\-e MYSQL\_ROOT\_PASSWORD=root123 \\

\-e MYSQL\_DATABASE=college \\

\-e MYSQL\_USER=admin \\

\-e MYSQL\_PASSWORD=admin123 \\

mysql:8



\## Explanation



\-d → Run container in background  

\-e → Set environment variables  



These variables are required for MySQL container to start.



Without these variables, MySQL container will fail to start.



\## Example: Check Variable Inside Container



docker run -it -e MY\_NAME=Sreekar ubuntu bash



Inside container:



echo $MY\_NAME



\## Notes



\- MY\_NAME exists only inside container

\- Host system is not affected



\## Using .env File (Professional Method)



Create .env file:



DB\_HOST=localhost

DB\_USER=root

DB\_PASS=secret



Run container:



docker run --env-file .env myapp



\## Interactive + Detached Mode Example



docker run -it -d httpd



Explanation:

\-it → interactive mode  

\-d → background mode  



Docker will pull image if not present and run container.



\## Summary



\- Environment variables are key-value pairs

\- Used for configuration and secrets

\- Multiple variables can be passed

\- .env file is best practice

