### install node
```
apt-get install nodejs
apt-get install npm
ln -s /usr/bin/nodejs /usr/bin/node
```

### install shadowsocks
```
apt-get install python-pip
pip install shadowsocks

vim /etc/shadowsocks.json

{
    "server":"你的服务器ip地址",
    "server_port":8388,
    "local_address": "127.0.0.1",
    "local_port":1080,
    "password":"你设置的密码",
    "timeout":300,
    "method":"aes-256-cfb",
    "fast_open": false
}

ssserver -c /etc/shadowsocks.json

#或者在后台运行
ssserver -c /etc/shadowsocks.json -d start
ssserver -c /etc/shadowsocks.json -d stop
```

### install jsbin
```
npm install -g jsbin
cd /usr/local/lib/node-modules/jsbin
cp config.default.json /etc/jsbin.config.json
$ JSBIN_CONFIG=/etc/jsbin.config.json jsbin
```
