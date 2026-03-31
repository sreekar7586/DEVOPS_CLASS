\# Day 7 - Environment Variables



Environment variables are used to configure containers dynamically.



\## Commands



docker run -e MY\_NAME=Sreekar ubuntu



\## Multiple Variables



docker run -e APP\_ENV=production -e VERSION=1 nginx



\## MySQL Example



docker run -d -e MYSQL\_ROOT\_PASSWORD=root mysql



\## Using env file



docker run --env-file .env myapp



\## Check variable



echo $MY\_NAME



\## Summary

Environment variables help manage configuration without modifying image.

