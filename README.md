# docker-nginx-load-balancer
Create a load balanced container cluster with Nginx and Docker.

The nginx.conf file in lb has 3 ip addresses for web1, web2 and web3.  Make sure you start the lb first so it gets the first ip address and then the web containers should get the next 3.  This also depends on your docker network including the default 172.17.0.0/24 network.

If you have a different network you will need to change the nginx.conf file.

Run the containers with the -d option so you don't have to open more than one terminal.

Use different ports mapping to port 80 on each container.  Ex: -p 8081:80
