---
layout: post
title: The powers of standard Windows accounts
comments: true
---

While running as a non-admin account is a sound and highly recommended security measure,
it is important to keep in mind that it should only be one layer of your security posture. 

It is very easy to underestimate the amount of damage that can be done by malware running as a standard Windows user.
Here is a quick roundup, which could hopefully serve as a refresher:

  * keylogging / password stealing 
  * file encryption (e.g., Cryptowall)
  * recording audio/video
  * banking trojan infections (e.g, Dridex) 
  * persistence (surviving reboots)
  * USB stick infections  
  * formatting external drives 
  * sending out any data  (outbound FW rules typically won't help much)
  * browser hijacking 
  * joining botnets
  * hosting illegal and/or darknet content  
  * serving a remote console (VNC)

In case I missed any other major risks, comments are welcome!

<A href=https://twitter.com/hexatomium>Follow</A> @hexatomium

View my <A HREF=https://www.linkedin.com/profile/view?id=1283234>LinkedIn</A> page (Firas Salem)
