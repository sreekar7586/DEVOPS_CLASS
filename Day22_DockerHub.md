\# Day 22 - Docker Hub and Image Management



Docker Hub is a cloud-based repository to store and share Docker images.



\## What is Docker Hub?



\- Public and private image repository

\- Used to store Docker images

\- Allows sharing across systems



\## Login to Docker Hub



docker login



Enter username and password.



\## Pull Image



docker pull nginx



Downloads image from Docker Hub.



\## Tag Image



docker tag myimage username/myimage:v1



\## Push Image



docker push username/myimage:v1



Uploads image to Docker Hub.



\## List Images



docker images



\## Remove Image



docker rmi <image\_id>



\## Force Remove



docker rmi -f <image\_id>



\## Example Workflow



1\. Create Dockerfile

2\. Build image

3\. Tag image

4\. Push to Docker Hub



\## Notes



\- Docker Hub is essential for deployment

\- Images can be reused across systems



\## Summary



Docker Hub helps in storing and sharing Docker images efficiently.

