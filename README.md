# MySQL + PMA on Docker
   Simply deploy Database Instance.
   
# Environment:
```
1. Linux
2. Docker ($ apt install -y nginx)
3. Docker Compose ($ apt install -y docker-compose)
```

# Deploy with Docker:
```
$ cd Docker-MySQL-PMA/
$ docker-compose up -d
$ docker ps (see container running)

Access on :
http://your_ip:3306 for MySQL
http://your_ip:8282 for phpmyAdmin
```

# Warning:
```
You can modified this simply template. 
And make sure you back up your database before dumping the container.
```
