---
layout: post
title: Microsoft silenty adds Amazon root certificates to its CTL
comments: true
---

Microsoft has just pushed a new CTL update with 6 new root certificates, 4 of which are for a brand new root CA: Amazon. 
This conveniently occurs just in time for Amazon's Certificate Services go-live. But what should be a fairly ordinary update is raising a few red flags. 

1. Unannounced by Microsoft. Their Program Participants page is oddly silent about the new roots.
   Additionally, it's interesting how Starfield (another root acquired by Amazon last year) does not appear in there either. 
   Probably just a coincidence, but I'll let you be the judge on that.

2. No other trust store provider (Mozilla, Google, Oracle) trusts these roots as of today.

3. Amazon appears to have some very close ties to spy agencies:
     http://www.defenseone.com/technology/2014/07/how-cia-partnered-amazon-and-changed-intelligence/88555/
     http://www.salon.com/2014/12/01/amazons_frightening_cia_partnership_capitalism_corporations_and_our_massive_new_surveillance_state/
     	 

<img src=http://i.imgur.com/b4Il9ff.png>
 
By the way, if you are running any supported version of Windows, be aware that you are already effectively trusting them now, even if you do not see them in the Windows Certificate Manager. 


<a href="http://twitter.com/share" class="twitter-share-button" 
data-url="http://hexatomium.github.io/2016/01/21/amazon-roots/" data-text="Microsoft silenty adds Amazon root certificates to its CTL"  data-count="horizontal">Tweet</a>
<script type="text/javascript" src="http://platform.twitter.com/widgets.js"></script>

<A href=https://twitter.com/hexatomium>Follow</A> @hexatomium
