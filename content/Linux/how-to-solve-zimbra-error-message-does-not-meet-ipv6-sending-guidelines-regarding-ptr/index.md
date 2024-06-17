---
title: "How to solve Zimbra error \"message does not meet IPv6 sending guidelines regarding PTR\""
date: "2022-08-22"
---

![](images/How-to-solve-Zimbra-error-message-does-not-meet-IPv6-sending-guidelines-regarding-PTR-1024x576.png)

[Zimbra Webpage](https://www.zimbra.com/) --- [zimbra](https://utho.com/docs/tutorial/how-to-install-zimbra-on-ubuntu-20-04-lts/)

**As we are using MTA hence i have logged in to MTA server and checked postfix inet protocol and found it was enabled for all**

Log into your server SSH and run the following commands:

```
root@mta:/etc/postfix# postconf inet_protocols
```  
```
inet_protocols = all
```

```
root@mta:/etc/postfix# postconf inet_protocols=ipv4
```  
```
root@mta:/etc/postfix# postconf inet_protocols
```  
```
inet_protocols = ipv4
```  
```
root@mta:/etc/postfix# service postfix restart
```  
```
root@mta:/etc/postfix# 
```

Thank you!
