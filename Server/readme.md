
# Server
- Web server (nginx, apache, micrsoft iis, light speed, tomcat)
- app server (node.js, tomcat)
- db server  (oracle, mongo)
- file server
- forward proxy (zscaler,squid, bluecoat) / Reverse Proxy (nginx)
- Cache server(redis, Memcached cache)
       |
       |---> cache hit and cache miss
  
---
## Nginx or Apache(httpd)

> cat /etc/os-release  # TO check the os version and linux flavour
> uname -a  #alternate way to check

### Installing nginx
Short way
- sudo su
- apt update -y
- apt install nginx -y

  or
Production way to follow proper documentation
url - nginx.org/en/linux_packages.html

### Nginx ++ load balancer
- nginx -v (check nginx version)
-`systemctl start nginx`
- `systemctl stop nginx`
- `systemctl restart nginx`
- `systemctl reload nginx`

- `nginx -t`  # To check the syntax od configuration file 

- To check the ruuning server:
  `curl localhost` or public id hit in browser or 127.0.0.1
- Add the multiple website to host also for DNS
  127.0.0.1 herolabs.internal

## Reference files
- Default.conf
- reverse_proxy.conf
- load-balancer.conf

 ### nginc env
- cd /etc/nginx #all configuration regarding nginx
- nginx.conf # uses file to run and follow (check include location of configuration)
- /conf.d (directory) or /sites-available (directory)     # these are the location whre server route
- cd /usr/share/nginx/html  # here you will able to keep all the file of the app or html data
- cd /var/log/nginx/access.log   # got logs
-  `ps -ef | grep nginx`   To check the master an worker node
-   also can able to change the LOG FORMAT and aatche the name in log
-   To check log `tail -f /var/log/nginx/access.log`
-   





Q. Server vs Client ? 
> server is like serving request (Nginx) and client is full app with db
> server is master node and client is slave node


