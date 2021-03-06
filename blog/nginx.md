### start / stop / restart

```
/etc/init.d/nginx start
/etc/init.d/nginx stop
/etc/init.d/nginx restart
```

### proxy

```
vim /etc/nginx/site-available/default

server {
      listen 80;
      server_name test.hostnam.com;
      location / {
            proxy_pass http://127.0.0.1:8081;
            proxy_set_header Host $host;
      }
}
```

### php
```
server {
    listen        80;
    server_name   test.hostnam.com;
    root          /home/uiteam/www;
    index         index.html index.php;

    location / {
            try_files $uri $uri/ /index.php$is_args$args;
    }
    location ~ \.php$ {
            fastcgi_pass   127.0.0.1:9000;
            fastcgi_index  index.php;
            fastcgi_param  SCRIPT_FILENAME  $document_root$fastcgi_script_name;
            include        fastcgi_params;
    }
```

### php-cgi
```
nohup php-cgi -b 9000 &
```

### php-fpm (php-cgi进程管理)
```
/etc/init.d/php-fpm start
/etc/init.d/php-fpm stop
/etc/init.d/php-fpm restart
```

### mysql
```
#先安装mysql在安装php
yum install mysql mysql-server
/etc/init.d/mysqld start 

#为root账户设置密码
mysql_secure_installation

yum install php 
yum install php-mysql 
```
