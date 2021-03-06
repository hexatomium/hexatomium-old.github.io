---
layout: post
title: The Executable Palindrome
comments: true
---

  What happens when you mix palindromes, a pinch of ASM, and a New Year hangover? 
  A tiny 600-byte *executable* binary palindrome :)

<img src=http://i.imgur.com/OXHphWP.png>

  This tiny Windows EXE will run identically even if all bytes are reversed.
  
  Of course it does not do much (actually all it does is exit with a specific return code) but
  it's a new type of palindrome, an executable palindrome.

  Also to make it a little more fun, one extra twist i added is to place the entry point (EP) in the mirrored half. Also, the actual executed code is contained *within* my New Year greetings :) 
  
  Building an executable palindrome part is actually simple. In fact, most EXEs can very easily be turned made into palindromes (with the possible exception of digitally signed EXEs.)

 Wanna give it a try?  Grab it from <A href=http://trax.x10.mx/download.php?appname=mzzm.exe>here</A> (or manually type in the above bytes using a hex editor, to experience a true hacker's high!)
  
 BTW, this would not have been possible without the awesome PE resources maintained by corkami.
   

<a href="http://twitter.com/share" class="twitter-share-button" 
data-url="http://hexatomium.github.io/2016/01/04/an-executable-palindrome/" data-text="MZZM - The 600-Byte Palindrome Executable"  data-count="horizontal">Tweet</a>
<script type="text/javascript" src="http://platform.twitter.com/widgets.js"></script>

<A href=https://twitter.com/hexatomium>Follow</A> @hexatomium
   
