# AWK 

### Get the shell installed

```
awk -F "/" '/^\// {print $NF}' /etc/shells | uniq
```

NF = last element


### Search and decode
```
for x in $(awk '/DB/ {print $NF}' cfg-credentials.yaml) ; do  echo "$x" | base64 -d ; done
```
