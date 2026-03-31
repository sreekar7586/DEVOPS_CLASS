\# Day 10 - Container Interaction



\## Exec Command



docker exec -it <container\_id> bash



\## Attach



docker attach <container\_id>



\## Copy Files



docker cp file.txt <container\_id>:/path



docker cp <container\_id>:/file .



\## Logs



docker logs <container\_id>

docker logs -f <container\_id>



\## Summary

Exec allows interaction with running container.

