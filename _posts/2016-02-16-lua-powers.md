---
layout: post
title: The privileges of standard Windows accounts
comments: true
---

While running as a non-admin account is a sound and highly recommended security measure,
it is important to keep in mind that it should only be one layer of your security posture. 

It is very easy to underestimate the amount of damage that can be done by malware running as a standard Windows user.
Here is a quick roundup:

  * password stealing (keylogging)
  * sending out any data / email (outbound FW rules won't help much)
  * file encryption (e.g., Cryptowall)
  * recording audio/video
  * getting a banking trojan infection (e.g, Dridex) 
  * persistence (surviving reboots)
  * USB stick infections  
  * formatting external drives 
  * browser hijacking 
  * joining botnets
  * hosting illegal and/or darknet content  
  * serving a remote console (VNC)

In case I missed any other interesting cases, comments are welcome!
