\# Day 37 - Kubernetes Pods and Deployments



Pods and Deployments are important Kubernetes objects.



\## What is a Pod?



A Pod is the smallest deployable unit in Kubernetes.



\- Contains one or more containers

\- Containers inside pod share:

&#x20; - Network

&#x20; - Storage



\## Create a Pod



kubectl run nginx-pod --image=nginx



\## View Pods



kubectl get pods



\## Pod Details



kubectl describe pod nginx-pod



\## Delete Pod



kubectl delete pod nginx-pod



\## What is a Deployment?



Deployment manages multiple pod replicas.



Features:

\- Scaling

\- Updates

\- Rollback

\- High availability



\## Create Deployment



kubectl create deployment myapp --image=nginx



\## View Deployments



kubectl get deployments



\## Scale Deployment



kubectl scale deployment myapp --replicas=3



\## Check Replica Sets



kubectl get rs



\## Expose Deployment



kubectl expose deployment myapp --port=80 --type=NodePort



\## Rolling Updates



Kubernetes supports rolling updates without downtime.



\## Advantages



\- Better scalability

\- Fault tolerance

\- Automated management



\## Notes



\- Pods are temporary

\- Deployments ensure desired state

\- Kubernetes automatically recreates failed pods



\## Summary



Pods run containers while deployments manage pod replicas and updates efficiently.

