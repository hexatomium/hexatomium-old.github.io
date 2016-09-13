---
layout: post
title: LastPass' password meter is broken 
comments: true
---
 
 Password strength meters are notoriously unreliable and LastPass is unfortunately no exception.
 Depending on what options are configured, the password strength meter inside the LastPass browser plugin, or at <a href=https://lastpass.com/generatepassword.php>lastpass.com</a> will give completely ridiculous estimates, providing a false sense of security. 
 <BR>
  **Example 1**
     <BR>
 Generating a purely numeric 14-digit password results in a green strength bar, although such a password is in fact extremely weak: with just 46 bits of entropy, it would be bruteforced in minutes by even a modest cracking rig.
<img src=http://trustprobe.com/images/lpgen.png>

    dict size: 10   length: 14  ->  46.50 bits of entropy  ->  bruteforce difficulty: trivial (minutes)

   <BR>
   **Example 2**
   <BR>   
   This password is shorter (10 characters) but results in an even longer and greener strength meter.

<img src=http://trustprobe.com/images/lpgen.png>
   
    dict size: 18   length: 10  ->  41.69 bits of entropy  ->  bruteforce difficulty: trivial (seconds)

  <BR><BR>
 So the bottom line is,  don't use LastPass to generate your passwords. At least not, until their fix their password meter.
 Don't get burned. Just use a proper, native password manager.
 
 PS. I had a rather bad experience reporting a previous (more serious) vulnerability to LastPass, so I'm not sure I want to go through that again.

<a href="http://twitter.com/share" class="twitter-share-button" 
data-url="http://hexatomium.github.io//2016/09/05/lastpass-password-meter-broken/" data-text="Don't use LastPass to generate your passwords"  data-count="horizontal">Tweet</a>
<script type="text/javascript" src="http://platform.twitter.com/widgets.js"></script>

<A href=https://twitter.com/hexatomium>Follow</A> @hexatomium
