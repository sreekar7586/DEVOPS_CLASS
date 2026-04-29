\# Day 29 - CI Pipeline with Docker using GitHub Actions



This demonstrates building and testing Docker images using CI/CD.



\## Objective



Automate Docker build process using GitHub Actions.



\## Workflow File Location



.github/workflows/docker.yml



\## Example Workflow



name: Docker CI



on:

&#x20; push:



jobs:

&#x20; build:

&#x20;   runs-on: ubuntu-latest



&#x20;   steps:

&#x20;     - name: Checkout Code

&#x20;       uses: actions/checkout@v2



&#x20;     - name: Build Docker Image

&#x20;       run: docker build -t myapp .



&#x20;     - name: Run Container

&#x20;       run: docker run -d -p 8080:80 myapp



\## Explanation



\- Trigger: runs on push

\- Job: build

\- Steps:

&#x20; - Checkout code

&#x20; - Build Docker image

&#x20; - Run container



\## Use Cases



\- Automated testing

\- Continuous deployment

\- DevOps pipelines



\## Advantages



\- No manual work

\- Faster deployment

\- Error detection early



\## Notes



\- Requires Dockerfile in repo

\- Runs on GitHub runner



\## Summary



GitHub Actions can automate Docker workflows for CI/CD pipelines.

