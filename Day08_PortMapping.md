\# Day 8 - Port Mapping



Port mapping allows external access to container applications.



\## Command



docker run -p 8080:80 nginx



\## Explanation

Host port 8080 → Container port 80



\## Without Port Mapping



docker run nginx



(Not accessible in browser)



\## Example



docker run -p 3000:80 nginx



\## Summary

\-p flag is used to expose container services.

