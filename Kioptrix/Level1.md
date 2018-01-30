---
layout: single
title: "VulnHub - Kioptrix 1"
header:
  overlay_image: kioptrix-banner.jpg
  caption: "[__VulnHub__](https://www.vulnhub.com/entry/kioptrix-level-1-1,22/)"
related: true
comments: true
---


## Description:
This Kioptrix VM Image are easy challenges. The object of the game is to acquire root access via any means possible (except actually hacking the VM server or player). The purpose of these games are to learn the basic tools and techniques in vulnerability assessment and exploitation. There are more ways than one to successfully complete the challenges.

## The Hack:
The first step that we need to do is to carry out some __Intelligence Gathering__. That includes [Footprinting](http://www.infosecwriters.com/text_resources/pdf/Footprinting.pdf) and [Fingerprinting](https://en.wikipedia.org/wiki/TCP/IP_stack_fingerprinting) hosts, servers, etc. If you want to learn more about the proper procedures and steps then I suggest you read the [PTES Technical Guidelines](http://www.pentest-standard.org/index.php/Main_Page).

Since the VM is being hosted on my Lab PC using a [Bridged Adapter](https://www.vmware.com/support/ws4/doc/network_bridged_ws.html) over VMWare, we will go ahead and scan our network to see if we can't get the IP address. To do so, type in `netdiscover` in your terminal.

```console
 Currently scanning: 172.24.166.0/16   |   Screen View: Unique Hosts           
                                                                               
 18 Captured ARP Req/Rep packets, from 4 hosts.   Total size: 1080             
 _____________________________________________________________________________
   IP            At MAC Address     Count     Len  MAC Vendor / Hostname      
 -----------------------------------------------------------------------------
 192.168.1.1     00:26:f2:0c:b3:82      4     240  NETGEAR                     
 192.168.1.4     d8:cb:8a:bf:d0:59      2     120  Micro-Star INTL CO., LTD.   
 192.168.1.13    18:03:73:1c:5d:6a     11     660  Dell Inc.                   
 192.168.1.104   00:0c:29:a8:19:5f      1      60  VMware, Inc.
```

