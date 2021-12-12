---
title: Codec and Video Encoding
updated: 2021-09-02 06:45:00
date: 2021-09-02 06:34:05
latitude: 30.29940000
longitude: 120.16120000
altitude: 0.0000
tags: Computer
---

`ffmpeg` yyds!

The size of the .h264 file is compressed to 1/10 of its original size, yet without significant compromise on quality.



hardware acceleration

```bash
ffmpeg -hwaccel qsv -c:v h264_qsv -noautorotate -i .\Al.mp4 -vcodec h264_qsv -f mp4 -s 1080x1080 Al_compressed.mp4
```

[ffmpeg转码使用硬件加速 - 水上云天 - 博客园](https://www.cnblogs.com/zzugyl/p/8439060.html)

What is `.h264` encoding? Why is its compression rate so high?

![46e91145849e3c27e33f67b5e350f0c9.png](./46e91145849e3c27e33f67b5e350f0c9.png)