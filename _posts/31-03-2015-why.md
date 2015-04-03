---
layout: post
title: Why excluding ANY file extensions in your antivirus is a Really Bad Idea
comments: true
---


It is often thought that some file extensions, such as TXT, INI, or LOG always indicate plain text files and cannot do any harm. This leads some people to configure exclusion rules to keep their AV from scanning these files.  

Here's an example that shows why doing so is dangerous. Here we have a Win32 executable disguised as a TXT file and bundled with a specially crafted LNK shortcut allowing the TXT file to be executed. If sent as an email attachment, non-savvy recipients can easily be tricked into unwillingly launching arbitrary code. (Not sure if this is worthy of a CVE or not, though)

<a href="http://imgur.com/1Eb1G57"><img src="http://i.imgur.com/1Eb1G57.png" title="source: imgur.com" /></a>


Link to the POC (This just opens a "Hello world" message box):  <A href=http://domain/files/poc_unzip_contents_to_desktop.zip>Download - 2.39 KB</A>


This seems to affect all Windows flavors, and was reported to Microsoft in October 2014, with no response so far.  In the meantime, do scan ALL your files, regardless of extension!
