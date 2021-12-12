---
title: SSH File Transfer
updated: 2021-09-05 15:21:25
date: 2021-09-05 12:55:57
latitude: 30.29940000
longitude: 120.16120000
altitude: 0.0000
tags: Computer
---

Windows SSH

```powershell
ssh Administrator@10.78.25.58
```

File transfer

```powershell
scp -r Administrator@10.78.25.58:/F:/Movies /F:/Movies/
```

~4 MB/s transfer rate, not bad for ZJUWLAN.

Even better, use `Filezilla`'s `sftp` (essentially `SSH` protocol) to resume transfer from break point

configuration like the image below.
![a86c363e88a44accd9889aae7a00b662.png](./a86c363e88a44accd9889aae7a00b662.png)