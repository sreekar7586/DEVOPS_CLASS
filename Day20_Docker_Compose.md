\# Day 20 - Docker Compose



Docker Compose is used to manage multi-container applications.



\## What is Docker Compose?



It allows you to define and run multiple containers using a YAML file.



\## Basic Command



docker compose up



Creates and starts containers.



\## Run in Background



docker compose up -d



\## Stop Services



docker compose stop



\## Start Services



docker compose start



\## Stop and Remove



docker compose down



Removes containers, networks, and volumes.



\## Build Images



docker compose build



\## Rebuild Containers



docker compose up --build



\## View Containers



docker compose ps



\## Logs



docker compose logs



docker compose logs -f



docker compose logs web



\## Execute Command



docker compose exec web bash



\## Run One-Time Command



docker compose run web command



\## Restart



docker compose restart



\## Pull Images



docker compose pull



\## Remove Stopped Containers



docker compose rm



\## Pause / Unpause



docker compose pause

docker compose unpause



\## View Configuration



docker compose config



\## Scale Services



docker compose up --scale web=3



\## Summary



Docker Compose simplifies managing multi-container applications efficiently.

