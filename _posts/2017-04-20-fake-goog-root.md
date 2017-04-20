---
layout: post
title: Rogue Google Root Certificates Seen in the Wild
comments: true
---

I've received user reports about a suspicious Google root certificate that my RCC scanner picked up on their Windows systems.  The details of the root cert are as follows:

    Sha1 thumbprint: 33FCD70343BBE07972D73CDEFDEB3C9F4DCEFE28 
    Validity: 2015-07-21 23:05:08 -> 2020-07-20 23:05:08 
    Usage: Enabled for all purposes

Checking against the official trust stores, it quickly became obvious this was a forged root certificate. 

After some more research I discovered a whole bunch of shady installers for popular software  
that have digital signatures chaining up to the above root.  A few examples include:

    MD5
    0b01e26a59e7c37089277b71a0fd1f62	Pepper_Flash_Player_19.0.0.185.plugin.paf.exe
    9e7ab1c2046f8af7f1c80ad8357accb1	officeportable_9.1.0.5217_multilingual_rev.4.paf.exe
    c4e9005a5ca9bf03f0d74cfe389ba120	JDownloaderPortable_2.0.paf.exe
    27236776af91c15d318422303ff610fe	EverythingPortable_x.x.x_32bit_64bit_Multilingual_Rev.1_online.paf.exe 
    3733bbb42d9d2c9c72f99ab33eb0e385  easeus data recovery wizard te x86+x64 9.5.0.paf.exe
    21d7c80baf93c2bc7fe896a10fc3b697	ChromePortable.exe


So far it seems the root has been primarily used to issue Authenticode certificates, but since it has all EKUs enabled, it could be misused to cause much more damage.
 
What I could not find out with my limited resources is how it gets added to the certificate stores of some PCs in the first place.

Be vigilant!

Note: Both Google and Microsoft security were notified. 
