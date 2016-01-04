---
layout: post
title: MZZM - The Palindrome Executable
comments: true
---


  What happens when you mix palindromes, tiny executables, and a New Year hangover? 

  This tiny (600-byte) Windows EXE will run identically even if all bytes are reversed:

<img src=http://i.imgur.com/OXHphWP.png>

  What's so special about this?
  It's a new type of palindrome, an executable palindrome.

  The palindrome part is actually simple. One little twist i added, to make it more fun, is to place the entry point (EP) in the mirrored section. Also, the code itself is contained within my New Year greetings :) 
  
  In fact, most existing EXEs can very easily be turned made into palindromes 
   (possible exceptions: digitally signed EXEs)

  
 Credits
   This would not have been possible without the awesome PE resources from corkami and bigmessofwires :)
   
