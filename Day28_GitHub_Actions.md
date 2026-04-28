\# Day 28 - CI/CD with GitHub Actions



CI/CD stands for Continuous Integration and Continuous Deployment.



\## What is CI/CD?



CI → Automatically builds and tests code  

CD → Automatically deploys code  



\## What is GitHub Actions?



\- Tool for automation inside GitHub

\- Runs workflows on events (push, pull request)



\## Key Components



Workflow → YAML file  

Job → Task  

Step → Individual command  

Runner → Machine that runs jobs  



\## Workflow File Location



.github/workflows/main.yml



\## Basic Example



name: CI Pipeline



on:

&#x20; push:



jobs:

&#x20; build:

&#x20;   runs-on: ubuntu-latest



&#x20;   steps:

&#x20;     - name: Checkout Code

&#x20;       uses: actions/checkout@v2



&#x20;     - name: Run Command

&#x20;       run: echo "Hello CI/CD"



\## Common Triggers



\- push

\- pull\_request

\- schedule



\## Use Cases



\- Build Docker images

\- Run tests automatically

\- Deploy applications



\## Advantages



\- Automation

\- Faster development

\- Reduced manual work



\## Notes



\- YAML syntax is important

\- Used in real DevOps pipelines



\## Summary



GitHub Actions helps automate build, test, and deployment processes.

