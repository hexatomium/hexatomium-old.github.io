---
layout: post
title: Windows 10 Lock Screen Leaks Clipboard Contents
comments: true
---

Earlier this year, Norwegian MVP <A HREF=https://twitter.com/Oddvarmoe>Oddvar Moe</A> made a rather shocking discovery that went mostly under the radar. On Windows 10, there is a way to read clipboard contents right from the lock screen, without any form of authentication. This would especially be a problem in enterprise environments, where any coworker could easily go through a few PCs at lunch time and harvest potentially juicy information (such as passwords) without leaving any traces.

The frighteningly simple PoC goes as follows:

    1. Win+L: Lock workstation
    2. Win+ENTER: Start Narrator
    3. CapsLock+F1: Open Narrator Help
    4. Ctrl+V: Profit!

By the way, this can also be achieved through the WiFi selector UI, right on the lock screen again.

The issue affects all editions of Windows 10. According to Moe, Microsoft does not consider this to be a security issue as it requires physical access.

Possible mitigations include disabling these features through the appropriate Group Policy settings, or using <A HREF=https://www.trustprobe.com/fs1/apps.html>ClipTTL</A>, which is a small utility I wrote to protect against this and other cases of accidental clipboard pasting (Do contact me before deploying ClipTTL in an enterprise environment).

**Update 2017-02-16** Windows 8.1 confirmed to be affected too.

<a href="https://twitter.com/share" class="twitter-share-button" 
data-url="https://hexatomium.github.io/2017/02/15/windows10-clipboard-lockscreen/" data-text="Windows 10 Leaks Clipboard Contents At The Lock Screen"  data-count="horizontal">Tweet</a>
<script type="text/javascript" src="https://platform.twitter.com/widgets.js"></script>
