\# Day 13 - Dockerfile Basics



Dockerfile is a text file used to create Docker images automatically.



\## What is Dockerfile?

It contains instructions to build a custom image.



\## Basic Syntax



\# comment

COMMAND argument



\## Important Commands



FROM ubuntu

RUN apt update

CMD \["echo", "Hello"]



\## Explanation



FROM → Base image  

RUN → Executes commands during build  

CMD → Default command when container starts  



\## Example Dockerfile



FROM ubuntu

RUN apt update

RUN apt install -y apache2

CMD \["echo", "Dockerfile example"]



\## Build Image



docker build -t myimage .



\## Run Image



docker run myimage



\## Additional Commands



WORKDIR /app

COPY . /app

ADD file /app

ENV NAME=Sreekar



\## Notes

\- Each instruction creates a layer

\- Dockerfile automates image creation



\## Summary

Dockerfile is used to create custom images efficiently.

