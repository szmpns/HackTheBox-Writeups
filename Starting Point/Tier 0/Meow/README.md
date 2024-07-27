# Meow      

![meow](./Screenshots/meowlogo.png)

## Solution

### Ping

When you want to test your connection to the target you can simply ping it:

![ping](./Screenshots/meowping.png)

### Scan with nmap

Type:

```
nmap -sV {target ip} -v
```

![nmap](./Screenshots/meownmap.png)

Port 23/tcp is open. The service is telnet.

### Telnet

Type:

```
telnet {target ip}
```

Use `root` as Meow login.

![telnet](./Screenshots/meowtelnet.png)

### Take the ls + cat

![ls+cat](./Screenshots/meowlscat.png)


![pwned](./Screenshots/meowpwned.png)

## Answers

### Task-1: What does the acronym VM stand for?

Virtual Machine

### Task-2: What tool do we use to interact with the operating system in order to issue commands via the command line, such as the one to start our VPN connection? It's also known as a console or shell.

terminal

### Task-3: What service do we use to form our VPN connection into HTB labs?

openvpn

### Task-4: What tool do we use to test our connection to the target with an ICMP echo request?

ping 

### Task-5: What is the name of the most common tool for finding open ports on a target?

nmap

### Task-6: What service do we identify on port 23/tcp during our scans?

telnet

### Task-7: What username is able to log into the target over telnet with a blank password?

root

### Submit root flag

Believe me, you can do that by yourself.