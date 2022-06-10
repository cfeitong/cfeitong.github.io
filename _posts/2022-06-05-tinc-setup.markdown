---
layout: post
title:  "用tinc做家庭内网穿透"
categories: linux network tinc
---

# tinc是什么呢？
tinc是一个用于vpn组网的小工具。在linux利用tun/tap设备，可以实现l2/l3层的组网。

# 用tinc解决什么问题？
目前家里的网络拓扑如下图所示，由于我租的自如，不好替换路由器，因此是没有公网ip的。为了从外网访问家里的设备，需要做个内网穿透。

# 外网服务器
做内网穿透，需要有个公网ip的服务器。这里不妨假设其公网ip为`124.32.41.152`，后称`server`。我们首先在`server`上配置tinc。tinc的配置文件目录总是`/etc/tinc/`，这个目录里放置着vpn网络名字的子目录，分别是各个vpn的配置。这里我们给vpn网络命名为tincvpn，那么相关的配置目录是`/etc/tinc/tincvpn`