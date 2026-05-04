\# Day 33 - Docker Image Inspection and History



Docker provides commands to inspect images and understand their structure.



\## 1. Docker Images Command



docker images



This command lists all available images with details:

\- Repository

\- Tag

\- Image ID

\- Created time

\- Size



\## 2. Docker Inspect



docker inspect nginx



This command shows detailed JSON information about an image or container.



Information includes:

\- Network settings

\- Mounts

\- Environment variables

\- Configuration



\## 3. Docker History



docker history nginx



Shows the history of image layers.



Details include:

\- Layer size

\- Commands used to build image

\- Creation time



\## Example Output Explanation



Each layer represents a step in Dockerfile.



Smaller layers → efficient image  

More layers → more storage  



\## 4. Docker Info



docker info



Provides system-wide Docker details:

\- Number of containers

\- Number of images

\- Storage driver

\- Kernel version



As shown in your notes, it displays running, stopped, and paused containers :contentReference\[oaicite:1]{index=1}



\## 5. Practical Example



docker pull nginx

docker images

docker history nginx

docker inspect nginx



\## Notes



\- Image inspection helps debugging

\- Useful in optimization

\- Important for production environments



\## Summary



Docker inspection commands help understand internal structure and behavior of images.

