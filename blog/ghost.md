## install

参考：<https://www.digitalocean.com/community/tutorials/how-to-create-a-blog-with-ghost-and-nginx-on-ubuntu-14-04>

```
    wget https://ghost.org/zip/ghost-latest.zip
    ...
    npm install --production
    ...
    vim config.js
    change the value of host in the server section to 0.0.0.0
    ...
    npm start --production
    ...
    done
```
