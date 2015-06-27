---
layout: post
title: Microsoft quietly pushes 17 new trusted root certificates
comments: true
---

Earlier this month, Microsoft has quietly started pushing a bunch of new root certificates to all supported Windows systems. What is concerning is that they did not announce this change in any KB article or advisory, and the security community doesn't seem to have noticed this so far. Even the official Microsoft Certificate Program member list makes no mention of these changes whatsoever. Are they really hoping to pull this off, or is it just incompetence? As some of these new certificates relate to rather 'brutal' regimes, or completely unknown authorities (RXC-R2? Now what the hell is that for a "friendly" name? Both the name and thumbprint are completely unknown on the Web at the time of this writing), color me very suspicious. 

Using my good old <A HREF=http://www.wilderssecurity.com/threads/rcc-check-your-systems-trusted-root-certificate-store.373819/>RCC</A> scanner (a root certificate auditing tool), I quickly identified the following certificates as new: 

      0f36385b811a25c39b314e83cae9346670cc74b4     GDCA TrustAUTH R5 ROOT         CN
      1b3d1114ea7a0f9558544195bf6b2582ab40ce9a     S-Trust Universal Root CA      DE
      1f3f1486b531882802e87b624d420295a0fc721a     Notarius Root CA               CA
      22fdd0b7fda24e0dac492ca0aca67b6a1fe3f766     Certplus Root CA G1            FR
      2c8affce966430ba04c04f81dd4b49c71b5b81a0     RXC-R2                         USA
      32f442093b36d7031b75ca4daddcb327faa02b9c     Swedish Government Root CA v2  SE
      3bc6dce00307bd676041ebd85970c62f8fda5109     CCA India 2015                 IN
      46af7a31b599460d469d6041145b13651df9170a     MULTICERT Root CA 01           PT
      4f658e1fe906d82802e9544741c954255d69cc1a     Certplus Root CA G2            FR
      6e2664f356bf3455bfd1933f7c01ded813da8aa6     OpenTrust Root CA G3           FR
      795f8860c5ab7c3d92e6cbf48de145cd11ef600b     OpenTrust Root CA G2           FR
      7991e834f7e2eedd08950152e9552d14e958d57e     OpenTrust Root CA G1           FR
      8094640eb5a7a1ca119c1fddd59f810263a7fbd1     GlobalSign Root CA - R6        US
      9638633c9056ae8814a065d23bdc60a0ee702fa7     Tunisian Root CA - TunRootCA2  TN
      a2b86b5a68d92819d9ce5dd6d7969a4968e11991     CCA India 2014                 IN
      d27ad2beed94c0a13cc72521ea5d71be8119f32b     WoSign ECC                     CN
      fbeddc9065b7272037bc550c9c56debbf27894e1     WoSign G2                      CN

 
I will update this post should new information surface.

<a href="http://twitter.com/share" class="twitter-share-button" 
data-url="http://hexatomium.github.io/2015/06/26/ms-very-quietly-adds-18-new-trusted-root-certs/" data-text="MS quietly pushes 18 root certificates"  data-count="horizontal">Tweet</a>
<script type="text/javascript" src="http://platform.twitter.com/widgets.js"></script>

<A href=https://twitter.com/hexatomium>Follow</A> @hexatomium 

View my <A HREF=https://www.linkedin.com/profile/view?id=1283234>LinkedIn</A> page


