# Trick to stay as king on KOTH from Tryhackme.
1. Method one
`
#!/bin/bash
while :
do
        eval "echo [usernameHere] >> /root/king.txt"
        eval " > /root/king.txt"
done
`
2. Method two
`while [[ $(cat /root/king.txt) != "[usernameHere]" ]]; do echo "[usernamehere]" >> /root/king.txt; done`
3. method three 
`* * * * * echo "[usernameHere]" >> /root/king.txt >/dev/null 2>&1`
