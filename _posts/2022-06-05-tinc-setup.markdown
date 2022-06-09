---
layout: post
title:  "用tinc做家庭内网穿透"
categories: linux network tinc
---

# tinc是什么呢？
tinc是一个用于vpn组网的小工具。在linux利用tun/tap设备，可以实现l2/l3层的组网。

# 用tinc解决什么问题？
目前家里的网络拓扑如下图所示，由于我租的自如，不好替换路由器，因此是没有公网ip的。为了从外网访问家里的设备，需要做个内网穿透。
