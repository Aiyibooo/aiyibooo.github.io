---
title: "SSH to Ubuntu from MacOS"
date: 2021-11-30T13:59:40+08:00
draft: false
---

## SSH to Ubuntu from mac


### Install ssh server on Ubuntu

```
sudo apt install ssh
```

### Generate key on MacOS

```
ssh-keygen
```


### Add public key to Ubuntu


#### On MacOS

Copy the flow command output

```
cat ~/.ssh/id_rsa.pub
```

#### On Ubuntu

Past the content to *~/.ssh/authorized_keys*.
If the file does not exist, create it first.

### Connect to Ubuntu on MacOS

```
ssh username@host
```

The host is your Ubuntu IP address or PC name.

### Disconnect

```
exit
```

## Use name for Ubuntu

If you don't want to type *ssh username@host*, you can add a name for SSH server.

### Modify SSH config on MacOS

Add the below content to *~/.ssh/config*. If the file does not exist, create it first.

```
Host xxx
    Hostname x.x.x.x
    User xxx
    Port 22
    IdentityFile ~/.ssh/id_rsa
```

- Replace 'xxx' after Host to the name you want.
- Replace 'x.x.x.x' fater Hostname to your Ubuntu IP address.
- Replace 'xxx' after User to your Ubuntu username.

For example

```
Host abc
    Hostname 192.168.1.123
    User louis
    Port 22
    IdentityFile ~/.ssh/id_rsa
```

### Connect to Ubuntu by short name on MacOS

```
ssh abc(the name after Host)
```
