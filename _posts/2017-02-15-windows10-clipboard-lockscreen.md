---
layout: post
title: Windows 10 Leaks Clipboard Contents At The Lock Screen
comments: true
---

Earlier this year a <A HREF=https://twitter.com/Oddvarmoe>Norwegian MVP</A> made a rather shocking discovery that went mostly under the radar. On Windows 10, there is a way to read clipboard contents right from the lock screen, without any form of authentication. This would especially be a problem in enterprise environments, where any coworker could easily go thru a few PCs at lunch time and harvest potentially juicy information (such as passwords) without leaving any traces.

The PoC goes as follows:

    1. Win+L: Lock workstation
    2. Win+ENTER: Start Narrator
    3. CapsLock+F1: Open Narrator Help
    4. Ctrl+V: Profit!

By the way, this can also be achieved through the WiFi selector UI, right on the lock screen again.

As of today, Microsoft has not released a fix for this issue, and it is not clear that they will.

Possible mitigations include disabling these options through the appropriate Group Policies settings, or using <A HREF=https://www.trustprobe.com/fs1/apps.html>ClipTTL</A>, which I wrote to protect against this and other cases of accidental clipboard pasting. (Do contact me before deploying ClipTTL in an enterprise environment).

<a href="https://twitter.com/share" class="twitter-share-button" 
data-url="https://hexatomium.github.io/2017/02/15/windows10-clipboard-lockscreen/" data-text="Windows 10 Leaks Clipboard Contents At The Lock Screen"  data-count="horizontal">Tweet</a>
<script type="text/javascript" src="https://platform.twitter.com/widgets.js"></script>
