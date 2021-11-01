
All the incoming and requests were first blocked.

``` sudo ufw default deny incoming 
    ssudo ufw default deny outgoing

```
Then,  only ssh was allowed in the firewall:

```
sudo ufw allow OpenSSH
```

