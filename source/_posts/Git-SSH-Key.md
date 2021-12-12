---
title: Git SSH Key
updated: 2021-08-24 14:33:04
date: 2021-08-24 13:57:30
latitude: 30.29400000
longitude: 120.16190000
altitude: 0.0000
author: Shaw Haines
tags: Computer
---


When I typed
```bash
git push origin dev
```

today on a remote computer, some error message showed up.

```bash
Support for password authentication was removed on August 13, 2021. Please use
 a personal access token instead.
```

See the [blogs by 廖雪峰](https://www.liaoxuefeng.com/wiki/896043488029600/896954117292416)

```bash
# if you don't know what it is doing, type:
# ssh-keygen --help
ssh-keygen -t rsa -C "youremail@example.com"
```

![f82d70ba7ca4e38232bd8920ab6bb96f.png](./f82d70ba7ca4e38232bd8920ab6bb96f.png)

![5ac19470ac08f05fd351241bc0ca8ccc.png](./5ac19470ac08f05fd351241bc0ca8ccc.png)

This is what a public key looks like

![f383afc50ff8b102369aa80ceb4cdcf1.png](./f383afc50ff8b102369aa80ceb4cdcf1.png)

If such error occurs:
```bash
fatal: unable to access 'https://github.com/xxx.git/': OpenSSL SSL_read: Connection was reset, errno 10054
```

set the term `sslVerify` to false.
```bash
git config --global https.sslVerify "false"
```

Error 443

```bash
fatal: unable to access 'https://github.com/xxx.git/': Failed to connect to github.com port 443: Timed out
```
The problem with proxy...

Install v2ray...

```bash
git config --global https.proxy http://127.0.0.1:1081
git config --global http.proxy http://127.0.0.1:1081
```