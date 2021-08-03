# Increase swap-memory

## show swap memory
```sh
free -m
```
-m mean memory unit is in MB


## Add 8gb swap memory

```sh
sudo fallocate -l 8G /swapfile1
sudo chmod 600 /swapfile1
sudo mkswap /swapfile1
sudo swapon /swapfile1
```
edit the `/etc/fstab`file with `sudo` in any editor
```sh
/swapfile1 swap swap defaults 0 0
```
copy and append in file

## result
```sh
sudo swapon --show
```

you see here your new created swap file

review your changes
```sh
free -m
```
