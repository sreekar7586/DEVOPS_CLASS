\# Day 16 - Dockerfile Advanced Commands



Dockerfile contains instructions to build custom images.



\## Important Commands



\### FROM

Defines base image



FROM ubuntu



\### WORKDIR

Sets working directory inside container



WORKDIR /app



If directory does not exist, Docker creates it.



\### COPY

Copies files from host to container



COPY . /app



\### ADD

Similar to COPY but can extract archives and download files



ADD file.tar.gz /app



\### RUN

Executes commands during build



RUN apt update \&\& apt install -y nginx



\### CMD

Default command when container starts



CMD \["echo", "Hello Docker"]



\### ENV

Sets environment variables



ENV APP\_ENV=production



\### EXPOSE

Exposes container port



EXPOSE 80



\## Example Dockerfile



FROM ubuntu

WORKDIR /app

COPY . /app

RUN apt update \&\& apt install -y nginx

CMD \["echo", "Dockerfile running"]



\## Build Image



docker build -t myimage .



\## Run Image



docker run myimage



\## Notes



\- Each command creates a new layer

\- Dockerfile automates image creation

\- WORKDIR improves organization



\## Summary



Dockerfile advanced commands help build efficient and reusable images.

