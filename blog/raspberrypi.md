# Raspbian

## install 
```
  diskutil list
  diskutil unmountDisk /dev/disk2
  sudo dd bs=1m if=2016-02-09-raspbian-jessie.img of=/dev/rdisk2
```

## No space left on device
```
  sudo raspi-config
  expend Filesystem
  restart
```
