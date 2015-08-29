---
layout: post
title: Why is Windows lying about what root certificates it trusts?
comments: true
---

Did you know? The Windows Certificate Trust List (aka CTL) is the master source that determines all the root certs your system ultimately trusts by default. In contrast, good old certmgr.msc only shows a much smaller subset of that list, which it proudly claims to be your system's "Trusted Root Certification Authorities". The real deal, though, is stored behind the scenes, in an obscure format, and Windows provides no GUI to view any information about it.

Starting with Windows Vista, a new AutoUpdate mechanism was added allowing these trusted root certificates to be invisibly downloaded on first use. 

Why does this matter? Because the incomplete information shown by Windows leads many people (including some security professionals) to believe that Windows trusts only a dozen or two root certificates out of the box, rather than hundreds. 

Here's a simple test:

 1. Open certmgr.msc, navigate to "Trusted Root Certification Authorities",  
    and notice the lack of a root called "OpenTrust Root CA G1" 
     
 2. Open IE or Chrome and navigate to https://certplusrootcag1-test.opentrust.com/ 
    Good, your browser could establish a trusted SSL connection!

 3. If you examine the SSL cert of that server, what do you notice?
    It's signed by root authority "OpenTrust Root CA G1", which WAS not in your store... 

 4. Open certmgr.msc again: now "OpenTrust Root CA G1" IS there and was added without any prompts. 
    Why? Because your system already trusted it via its CTL. 

 5. Bottom line? Certmgr.msc is not showing the whole picture. 
    In fact, there's no GUI view anywhere in the OS that shows any detail on the CTL. 
  

<A href=http://trax.x10.mx/apps.html>CTLInfo</A>

CTLInfo is the result of a few sleepless nights spent understanding and reverse engineering 
some of the CTL obscure format. (If someone knows where to find detailed specs on that format, 
I'd love to hear from you!) It is a very small tool showing some key information about your 
system's CTL. I made this as I simply could find no other way for the end-user to get this sort of information.



<!-- <a href="http://twitter.com/share" class="twitter-share-button" 
data-url="http://hexatomium.github.io/2015/06/26/ms-very-quietly-adds-18-new-trusted-root-certs/" data-text="MS quietly pushes 17 root certificates"  data-count="horizontal">Tweet</a>
<script type="text/javascript" src="http://platform.twitter.com/widgets.js"></script>  -->

<A href=https://twitter.com/hexatomium>Follow</A> @hexatomium

View my <A HREF=https://www.linkedin.com/profile/view?id=1283234>LinkedIn</A> page (Firas Salem)
