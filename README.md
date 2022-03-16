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

# Increase PMA Import Size
```
$ docker inspect phpmyadmin
---
"MergedDir": "/var/lib/docker/overlay2/e703e63ddf58c0decebd292eabaf8fe2c7eef49eafa390d7f7cc971f523fb0a8/merged",
---

$ cd var/lib/docker/overlay2/e703e63ddf58c0decebd292eabaf8fe2c7eef49eafa390d7f7cc971f523fb0a8/merged
$ nano usr/local/etc/php/conf.d/phpmyadmin-misc.ini

Add 2 lines :
---
upload_max_filesize = 1024M
post_max_size = 1024M
---

$ docker restart phpmyadmin
```

# Warning:
```
You can modified this simply template. 
And make sure you back up your database before dumping the container.
```
