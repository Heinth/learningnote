# How to change nginx default port in ubuntu

```text
vi /etc/nginx/sites-enabled/default
#Change Listen port
listen 3200 default_server;
```

After that we need to restart nginx service.

```text
systemctl restart nginx 
netstat -tlpn | grep nginx
```

