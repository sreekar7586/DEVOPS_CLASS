\# Day 40 - Jenkins and Docker Integration



Jenkins can integrate with Docker to automate container-based workflows.



\## Why Integrate Jenkins with Docker?



Benefits:

\- Automated image building

\- Consistent environments

\- Faster deployment

\- CI/CD automation



\## Jenkins + Docker Workflow



1\. Developer pushes code to GitHub

2\. Jenkins detects changes

3\. Jenkins builds Docker image

4\. Jenkins runs tests

5\. Jenkins pushes image to Docker Hub



\## Run Jenkins using Docker



docker run -d \\

\-p 8080:8080 \\

\-p 50000:50000 \\

jenkins/jenkins:lts



\## Install Docker Plugin in Jenkins



Steps:

1\. Open Jenkins Dashboard

2\. Manage Jenkins

3\. Plugins

4\. Install Docker plugin



\## Jenkinsfile Example



pipeline {



&#x20;   agent any



&#x20;   stages {



&#x20;       stage('Build Docker Image') {

&#x20;           steps {

&#x20;               sh 'docker build -t myapp .'

&#x20;           }

&#x20;       }



&#x20;       stage('Run Container') {

&#x20;           steps {

&#x20;               sh 'docker run -d -p 8080:80 myapp'

&#x20;           }

&#x20;       }

&#x20;   }

}



\## Push Docker Image to Docker Hub



docker login



docker tag myapp username/myapp:v1



docker push username/myapp:v1



\## Advantages



\- Automated deployment

\- Continuous Integration

\- Faster software delivery

\- Easy container management



\## Notes



\- Docker daemon must be running

\- Jenkins requires Docker access

\- Common in DevOps pipelines



\## Summary



Jenkins and Docker together automate build, test, and deployment workflows efficiently.

