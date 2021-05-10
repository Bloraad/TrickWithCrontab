# Trick to stay as king on KOTH from Tryhackme.
>1. Method one
```
#!/bin/bash
while :
do
        eval "echo qccq >> /root/king.txt"
        eval " > /root/king.txt"
done
```
> 2. Method two

```
while [[ $(cat /root/king.txt) != "qccq" ]]; do echo "[qccq]" > /root/king.txt; done
```

> 3. Method three 
```
* * * * * echo "qccq" >> /root/king.txt >/dev/null 2>&1
```
> 4. Method four
```
LFILE=/root/king.txt
echo "qccq" | cp /dev/stdin "$LFILE"
```
