### samba安装 
yum inatall samba 
 
### samba配置 
vim /etc/samba/smb.conf
/etc/init.d/smb start 
/etc/init.d/nmb start 
 
### samba用户管理 
添加系统用户 
添加samba用户 smbpasswd -a username
