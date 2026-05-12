\# Day 39 - Jenkins Pipeline and Jenkinsfile



Jenkins Pipeline automates software delivery using stages.



\## What is Jenkins Pipeline?



A pipeline is a series of automated steps:

\- Build

\- Test

\- Deploy



Pipelines are written using Jenkinsfile.



\## Types of Pipelines



1\. Declarative Pipeline

2\. Scripted Pipeline



Declarative is simpler and commonly used.



\## What is Jenkinsfile?



A text file containing pipeline code.



Stored inside project repository.



\## Basic Jenkinsfile Example



pipeline {



&#x20;   agent any



&#x20;   stages {



&#x20;       stage('Build') {

&#x20;           steps {

&#x20;               echo 'Building Application'

&#x20;           }

&#x20;       }



&#x20;       stage('Test') {

&#x20;           steps {

&#x20;               echo 'Running Tests'

&#x20;           }

&#x20;       }



&#x20;       stage('Deploy') {

&#x20;           steps {

&#x20;               echo 'Deploying Application'

&#x20;           }

&#x20;       }

&#x20;   }

}



\## Pipeline Stages



\### Build Stage

Compiles application.



\### Test Stage

Runs automated tests.



\### Deploy Stage

Deploys application to server.



\## Advantages



\- Automation

\- Faster delivery

\- Error reduction

\- Continuous Integration



\## Jenkins Pipeline Commands



\- Build Project

\- Run Tests

\- Deploy Containers



\## Integration with GitHub



Jenkins can:

\- Pull code from GitHub

\- Trigger builds automatically



\## Notes



\- Jenkinsfile uses Groovy syntax

\- Pipelines improve DevOps workflow

\- Supports Docker integration



\## Summary



Jenkins Pipelines automate build, test, and deployment processes efficiently.

