---
layout: post
title: 14 new trusted root certificates added to Windows in unannounced update
comments: true
---


My monitoring scripts raised an alert a few days ago: Microsoft has just quietly updated its Root CTL (Certificate Trust List), increasing its size to 356 roots.

The <a href=http://social.technet.microsoft.com/wiki/contents/articles/31680.microsoft-trusted-root-certificate-program-updates.aspx>official</a> <A href=http://social.technet.microsoft.com/wiki/contents/articles/31634.microsoft-trusted-root-certificate-program-participants-v-2016-april.aspx>channels</a>, which normally announce and document such updates well in advance, are oddly silent about this one, and the new CTL is already being pushed to all Windows systems (including servers). 

A quick <A HREF=https://www.wilderssecurity.com/threads/rcc-check-your-systems-trusted-root-certificate-store.373819/>RCC</A> scan (shameless plug!) highlights the following entries as new: 

    1e0e56190ad18b2598b20444ff668a0417995f3f	LU    LuxTrust Global Root 2
    5463283b6793ff55277cede39098e80422f912f7	CO    AC Raiz Certicamara S.A.
    3143649becce27eced3a3f0b8f0de4e891ddeeca	TR    TUBITAK Kamu SM SSL Kok Sertifikasi  Surum 1
    e252fa953feddb2460bd6e28f39ccccf5eb33fde	HR    SZAFIR ROOT CA2
    3f0feb17a7ef5804cfd90a77b7bb021ea69c6418	GR    BYTE Root Certification Authority 001
    a69e0336c4e59023ff653c71f928eb73f21c00f0	CA    Carillon Information Security Inc.
    d99b104298594763f0b9a927b79269cb47dd158b	TW    ePKI Root Certification Authority - G2
    81ac5de150d1b8de5d3e0e266a136b737862d322	TW    ePKI Root Certification Authority - G2
    c3197c3924e654af1bc4ab20957ae2c30e13026a	US	  SSL.com Root Certification Authority ECC
    b7ab3308d1ea4477ba1480125a6fbda936490cbb	US    SSL.com Root Certification Authority RSA
    4cdd51a3d1f5203214b0c6c532230391c746426d	US    SSL.com EV Root Certification Authority ECC
    1cb7ede176bcdfef0c866f46fbf980e901e5ce35    US    SSL.com EV Root Certification Authority RSA
    d3dd483e2bbf4c05e8af10f5fa7626cfd3dc3092	PL    Certum Trusted Network CA 2
    d496592b305707386cc5f3cdb259ae66d7661fca	ES    ACA ROOT

Trusting new CAs is always a big deal, so advanced users and enterprise admins may use the above list to research these new roots and decide which ones they actually want to trust.  And I'm currently working on a trust store hardening product, which will make it easy to drastically reduce your exposure to unnecessary CAs. Stay tuned! 

**Update** 13-Oct-2016: Microsoft confirms the <a href=http://social.technet.microsoft.com/wiki/contents/articles/31634.microsoft-trusted-root-certificate-program-participants.aspx>release</a>.

<a href="https://twitter.com/share" class="twitter-share-button" 
data-url="https://hexatomium.github.io/2016/10/11/unannounced-root-cert-update/" data-text="14 new trusted root certificates added to Windows in unannounced update"  data-count="horizontal">Tweet</a>
<script type="text/javascript" src="https://platform.twitter.com/widgets.js"></script>

<A href=https://twitter.com/hexatomium>Follow</A> @hexatomium for more updates and the occasional crazy thought.
