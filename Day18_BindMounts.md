\# Day 18 - Bind Mounts and --mount



Bind mounts allow linking host files directly with container.



\## Difference from Volume



Volume → managed by Docker  

Bind Mount → uses host filesystem  



\## Example (Bind Mount)



docker run -it -v C:/data:/app ubuntu bash



\## Explanation



C:/data → host folder  

/app → container folder  



\## Real-time Sync



Changes in host reflect inside container instantly.



\## Example with Nginx



docker run -it --rm --name nginx \\

\-p 8080:80 \\

\-v "$(pwd)":/usr/share/nginx/html nginx



\## Test



Create file in host:



echo "<h1>Hello</h1>" > index.html



Open browser:

http://localhost:8080



\## Using --mount (Modern Way)



docker run --mount type=bind,source=C:/data,target=/app ubuntu



\## Notes



\- Bind mounts depend on host path

\- Useful for development

\- Real-time updates



\## Summary



Bind mounts allow sharing data between host and container.

