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

Past the content to *~/.ssh/authorized_keys*

