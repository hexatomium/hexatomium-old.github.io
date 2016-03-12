---
layout: post
title: Cheatsheet - The powers of "limited" Windows accounts
comments: true
---

While using a non-admin account for everyday tasks is a sound and highly recommended security measure,
it is important to keep in mind that it should only be one layer of your security posture. 

It is easy to underestimate the amount of damage that can be done by malware running as a "limited" Windows user, even without resorting to privilege escalation. Here is a quick roundup:

  1.   keylogging / password stealing 
  2.   file encryption (e.g. Cryptowall)
  3.   silently recording audio/video
  4.   banking trojan infections (e.g. Dridex) 
  5.   persistence (surviving reboots)
  6.   formatting external FAT drives  
  7.   infecting USB sticks 
  8.   sending out any data  (outbound FW rules typically won't help much)
  9.   browser hijacking 
  10.  joining a botnet
  11.  hosting content  
  12.  reading memory of other processes (e.g. Keepass)  
  13.  serving a remote console (e.g. VNC)
  14.  port scanning / network recon
  15.  Active Directory enumeration

Did you know you all of the above could be done with a regular account? 

<A href=https://twitter.com/hexatomium>Follow</A> @hexatomium

View my <A HREF=https://www.linkedin.com/profile/view?id=1283234>LinkedIn</A> page (Firas Salem)
