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
            root           /home/uiteam/www;
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
