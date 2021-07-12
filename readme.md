# Explanation #
>There are two services. One service is that the port is open, which implies that anyone can respond to it. Another service is running, but the port is closed. When a user requests something, it's usually a GET request. So, when I access the external service port, which is 8081, I notice that my API is operational. Each and every container is isolated from each other and they only connected through bridge. No container communicates internally. I tried the follwing code and tried to find out the internal container IP and PORT number and and edit it to internalURL of index file.  


# service to service Communication #
> docker system prune -a
> 
> git clone https://github.com/iftekharchowdhury/node-ec2.git

>docker build --no-cache -t internal .
* Builing Container

>docker run -d -p 80:80 internal
* Container Run

>docker inspect ce30
* To find out the Ip for internal Service 

>docker build --no-cache -t external .

>docker run -d -p 8081:8081 external

*Crated new directory to upload it to github*


**Create New Repository**
>mkdir node-service

>echo "# node-service" >> README.md

>git init

>git add README.md

>git commit -m "first commit"

>git branch -M main

>git remote add origin https://github.com/SanjidMahmud/node-service.git

>git push -u origin main

>cp -R External/ ~/node-service

>cp -R Internal/ ~/node-service

>git add .

>git commit -m "External & Internal Folder Added"

>git push

# Communication between External & Internal Service #
> Find the get reponse here

`http://13.229.155.102:8081/api/v1/add` 

`http://13.229.155.102:8081/status`

    
