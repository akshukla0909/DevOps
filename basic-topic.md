1 ) Basics of server setup ( DevOps )

2 ) Hosting services 
    -> Shared
    -> VPS
    -> Dedicated
    -> Serverless
    -> Managed

3 ) Web Servers ( NGINX, Caddy, Traefik, Apache )
    -> Static 
    -> Dynamic
    -> Reverse Proxy 

4 ) DNS Records

5 ) AWS
    -> IAM
    -> Regions
    -> Some services

6 ) Docker Basics
    -> Images - Prototype
    -> Containers - 
    -> Volumes - 
    -> Networks - 
    -> HUB & ECR

Setting up project 
----------------
-> git clone
-> node installation
-> mongodb // optional 
-> npm i
-> npm run build 
-> npm run server
-----------------


-----------------
Servers 
-----------
1 PC 20GB - 10 VirtualMachine 2GB - 1  -> 3 customer ----> SHARED 
1 PC 20GB - 10 VirtualMachine 2GB - 1  -> 1 customer ----> VPS
1 PC 20GB ----> DEDICATED 
1 PC 20GB - MANAGED


----------
Server -> VPS -> project setup -> localhost is listening on 3000 port -> 192.123.112.12

proxy 
reverse-proxy 
80
443
-----------
DNS
----------
A type api.eisele.com 192.123.112.12 TTL : 300
A type app.eisele.com 192.123.112.12 TTL : 300
TXT type
------------