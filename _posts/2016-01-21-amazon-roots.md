---
layout: post
title: Microsoft silenty adds Amazon root certificates to its CTL
comments: true
---

Microsoft has just pushed a new CTL update with 6 new root certificates, 4 of which are for a brand new root CA: Amazon. 
This conveniently occurs just in time for Amazon's Certificate Services go-live. But what should have been a fairly ordinary update is raising a few red flags. 

1. Amazon is reported to have some <a href=http://www.defenseone.com/technology/2014/07/how-cia-partnered-amazon-and-changed-intelligence/88555/>close ties</a> to <a href=http://www.salon.com/2014/12/01/amazons_frightening_cia_partnership_capitalism_corporations_and_our_massive_new_surveillance_state/>spy agencies</a>.

2. The new roots have not been announced by Microsoft. Their <A Href=http://social.technet.microsoft.com/wiki/contents/articles/31634.microsoft-trusted-root-certificate-program-participants.aspx>Program Participants</A> page is oddly silent about the changes.
   Additionally, it's interesting that Starfield (another root acquired by Amazon last year) does not appear in there either. 
   Hopefully that's just a coincidence  - I will not to speculate on that.

3. No other trust store provider (Mozilla, Google, Oracle) trusts these roots as of today.

<a href=http://trax.x10.mx/apps.html>RCC</A> detecting the new roots:

<img src=https://i.imgur.com/b4Il9ff.png>
 
By the way, if you are running any supported version of Windows, be aware that you are already effectively trusting them now, <a href=http://hexatomium.github.io/2015/08/29/why-is-windows/>even if you do not see them in the Windows Certificate Manager</a>. 


<a href="http://twitter.com/share" class="twitter-share-button" 
data-url="http://hexatomium.github.io/2016/01/21/amazon-roots/" data-text="Microsoft silenty adds Amazon root certificates to its CTL"  data-count="horizontal">Tweet</a>
<script type="text/javascript" src="https://platform.twitter.com/widgets.js"></script>

<A href=https://twitter.com/hexatomium>Follow</A> @hexatomium
