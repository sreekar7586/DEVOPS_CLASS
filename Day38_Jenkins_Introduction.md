\# Day 38 - Introduction to Jenkins



Jenkins is an open-source automation server used for CI/CD pipelines.



\## What is Jenkins?



Jenkins automates:

\- Build

\- Testing

\- Deployment



It helps developers deliver applications faster.



\## Why Jenkins?



Manual deployment is:

\- Slow

\- Error-prone

\- Difficult to manage



Jenkins automates the process.



\## Jenkins Architecture



1\. Master Node

\- Controls Jenkins

\- Schedules jobs



2\. Agent Node

\- Executes jobs



\## Features



\- Continuous Integration

\- Continuous Deployment

\- Plugin support

\- Pipeline automation



\## Installation Methods



\- Docker

\- Windows installer

\- Linux package



\## Run Jenkins using Docker



docker run -d \\

\-p 8080:8080 \\

\-p 50000:50000 \\

jenkins/jenkins:lts



\## Access Jenkins



Open browser:



http://localhost:8080



\## Initial Setup



\- Unlock Jenkins

\- Install suggested plugins

\- Create admin user



\## Jenkins Jobs



A job is a task executed by Jenkins.



Examples:

\- Build Java project

\- Run tests

\- Deploy application



\## Advantages



\- Automation

\- Faster software delivery

\- Reduced manual work

\- Better testing



\## Notes



\- Jenkins supports many plugins

\- Commonly used in DevOps pipelines

\- Integrates with GitHub and Docker



\## Summary



Jenkins automates software build, testing, and deployment processes efficiently.

