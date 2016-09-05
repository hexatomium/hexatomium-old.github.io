---
layout: post
title: Don't use LastPass to generate your passwords 
comments: true
---
 
 Don't use LastPass to generate your passwords. Or if you do, do not trust the handy strength meter.
 
 <img src=http://trustprobe.com/images/lpgen.png>
 
 Password stregth meters are notoriously unreliable and LastPass is unfortunately no exception.
 Depending on what options are configured, the password strength meter inside the LastPass browser plugin, or at https://lastpass.com/generatepassword.php will give completely misleading estimates. For instance, generating a purely numeric 14-digit password results in a green strength bar, although such a password is in fact extremely weak: with just 46 bits of entropy, it would be bruteforced in minutes by even a modest cracking rig. 
 Don't get burned. Use a proper, native password manager.
 

<a href="http://twitter.com/share" class="twitter-share-button" 
data-url="http://hexatomium.github.io//2016/09/05/lastpass-password-meter-broken/" data-text="Don't use LastPass to generate your passwords"  data-count="horizontal">Tweet</a>
<script type="text/javascript" src="http://platform.twitter.com/widgets.js"></script>

<A href=https://twitter.com/hexatomium>Follow</A> @hexatomium
