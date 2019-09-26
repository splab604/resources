# User Admin
## create user
```
sudo adduser --home /data/zhangsan zhangsan
cd /data & chmod –R 700 zhangsan
```

## create shareable folder
```
sudo system-config-samba 
```

## delete user and data
```
# 1. delte samba user first
sudo system-config-samba
# 2. delete user
sudo deluser zhangsan
# 3. delete user data
sudo rm –rf /data/zhangsan
```
