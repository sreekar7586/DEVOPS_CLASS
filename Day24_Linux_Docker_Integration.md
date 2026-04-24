\# Day 24 - Linux Commands with Docker



Linux commands are essential for working inside Docker containers.



\## Basic Linux Commands



\### List files



ls

ls -l

ls -a



\### Change directory



cd /app



\### Create file



touch file.txt



\### Write content



cat > file.txt



\### View file



cat file.txt



\## Directory Commands



mkdir myfolder

rmdir myfolder



\## Remove files



rm file.txt

rm -r folder



\## Copy and Move



cp file1 file2

mv file1 file2



\## Search using grep



cat file.txt | grep word



\## Find files



find . -name file.txt



\## Run Linux Commands Inside Docker



docker run -it ubuntu bash



\## Example Workflow



1\. Run container



docker run -it ubuntu bash



2\. Create file



touch test.txt



3\. Add content



echo "Hello Docker Linux" > test.txt



4\. View file



cat test.txt



\## Using docker exec



docker exec -it <container\_id> bash



\## Notes



\- Linux commands are used inside containers

\- Containers behave like Linux systems

\- Essential for DevOps tasks



\## Summary



Linux commands combined with Docker help manage containers effectively.

