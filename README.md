# Linux tricks

**Delete untagged docker images**
```
docker rmi $(docker images | grep "^<none>" | awk '{print $3}')
```

**Delete all docker images**
```
docker rmi -f $(docker images -q)
```

**Delete dangling docker volumes**
```
docker volume ls -qf dangling=true | xargs -r docker volume rm
```

**View largest folders in current folder**
```
sudo du -hsx * | sort -rh | head -10
```

**Restart VBoxClient**
```
killall VBoxClient
VBoxClient-all
```

