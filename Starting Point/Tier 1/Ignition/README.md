# Ignition      

![Ignition](./Screenshots/ignitionlogo.png)

## Solution

### Scan with nmap

Type:

```
nmap -sC -sV {target ip} -v
```

![nmap](./Screenshots/ignitionnmap.png)

`80/tcp` is open. Service is `http`.

#### Disclaimer

![Disclaimer](./Screenshots/ignitiondisclaimer.png)

As the nmap scan says `http-title: Did not follow redirect to http://ignition.htb/`, I would recommend adding `{target ip} ignition.htb` into your `/etc/hosts` file.

To do this type:

```
sudo nano /etc/hosts
```

At the very end paste section from above and `save` it. You can do that by `Ctrl + X`. Then press `Y`.

![Disclaimer](./Screenshots/ignitiondisclaimer2.png)

After pasting `target ip` into the browser we can see the website.

![web](./Screenshots/ignitionweb.png)

### gobuster

Type:

```
gobuster dir -u http://ignition.htb/ -w {path to dictionary you want to use}
```

`dir` - Specifies the mode of Gobuster to use, in this case, directory brute-forcing.

`-u` - Specifies the target URL to scan.

`-w` - Specifies the wordlist to use for the directory brute-forcing.

![Gobuster](./Screenshots/ignitiongobuster.png)

We found `admin` login panel.

```
http://ignition.htb/admin
```

![admin](./Screenshots/ignitionadmin.png)

I found it on the Internet that default `Magento` admin credentials are:

```
admin:123123
```

![admin](./Screenshots/ignitionadmin2.png)

Let's try this combination.

![admin](./Screenshots/ignitionadmin3.png)

It haven't worked.

### Burpsuite

As only one port is open - `80/tcp`, the only reasonable option is to brute force the password.

Usually the administrator's username is not changed, so since default `Magento` credentials are not working, focusing on password seems smart.

Let's intercept the `login request`:

![Burpsuite](./Screenshots/ignitionburp.png)

Send it to `Intruder` by pressing `Ctrl + I`.

![Burpsuite](./Screenshots/ignitionburp2.png)

Now, select the password payload which you provided and press `Add §`.

![Burpsuite](./Screenshots/ignitionburp3.png)

Next, in the `Payloads` section `load` wordlist of passwords you want to try.

![Burpsuite](./Screenshots/ignitionburp4.png)

If it's done, press `Start attack`.

![Burpsuite](./Screenshots/ignitionburp5.png)

We found the `password`. It's `qwerty123`.

### Get the flag

Let's login.

![flag](./Screenshots/ignitionflag.png)

The flag is displayed on the dashboard.

![flag](./Screenshots/ignitionflag2.png)

### Paste the flag

![pwned](./Screenshots/ignitionpwned.png)

## Answers

### Task-1: Which service version is found to be running on port 80?

nginx 1.14.2

### Task-2: What is the 3-digit HTTP status code returned when you visit http://{machine IP}/?

302

### Task-3: What is the virtual host name the webpage expects to be accessed by?

ignition.htb

### Task-4: What is the full path to the file on a Linux computer that holds a local list of domain name to IP address pairs?

/etc/hosts

### Task-5: Use a tool to brute force directories on the webserver. What is the full URL to the Magento login page?

http://ignition.htb/admin

### Task-6: Look up the password requirements for Magento and also try searching for the most common passwords of 2023. Which password provides access to the admin account?

qwerty123

### Submit root flag

Good one.