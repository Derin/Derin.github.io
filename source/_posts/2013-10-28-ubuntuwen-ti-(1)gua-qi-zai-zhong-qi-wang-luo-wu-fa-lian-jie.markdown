---
layout: post
title: "ubuntu问题（1）挂起再重启网络无法连接"
date: 2013-10-28 16:23
comments: true
categories: 
---
##问题描述：
在ubuntu系统下使用 `< 挂起 >` 功能，再重新唤醒系统后，发现网络无法使用，并且再点击 `< 网络 >` 中的 `< 启动联网 >` 仍然无法使用。

##解决方法：
- 修改'<\etc\default\acpi-support>' 文件

    sudo vim \etc\default\acpi-support

将其中的 `STOP_SERVICES=` 改为 `STOP_SERVICES="networking"`