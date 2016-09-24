---
layout: post
title:  Windows 10 has an undocumented certificate pinning feature 
comments: true
---
 
After getting to play with Windows 10 for a few hours, something unexpected caught my attention.
  
<img src=http://i.imgur.com/7MJQmGV.png>

Hey, there's some new stuff in there - a third, undocumented CTL! <BR>
Googling for 'PinRulesEncodedCtl' turned up nothing at all. The first few bytes of the binary data (30 82 .. .. 06 09 2a 86 48) looked familiar: it was probably ASN.1 encoded data, just like the other two CTLs. That meant I could probably just feed it into my existing tools for a painless decoding.

Success! We get a nice list of 152 Microsoft-owned domains.
   
    Subject Identifier: .files-df.1drv.com
    Subject Identifier: .files.1drv.com
    Subject Identifier: .aadrm.com
    Subject Identifier: .afx.ms
    Subject Identifier: .akadns.net
    Subject Identifier: .aspnetcdn.com
    Subject Identifier: .azure-int.net
    Subject Identifier: .azure-mobile.net
    Subject Identifier: .azure.com
    Subject Identifier: .cloudapp.azure.com
    Subject Identifier: azure.com
    Subject Identifier: .azure.net
    Subject Identifier: .cloudapp.azure.net
    Subject Identifier: .azureedge.net
    Subject Identifier: .azurewebsites.net
    Subject Identifier: .bing-exp.com
    Subject Identifier: .bing-int.com
    Subject Identifier: .bing.com
    Subject Identifier: bing.com
    Subject Identifier: download.cortana.cn.bing.com
    Subject Identifier: .bing.net
    Subject Identifier: .ceipmsn.com
    Subject Identifier: .cloudapp.net
    Subject Identifier: .codeplex.com
    Subject Identifier: .discoverbing.com
    Subject Identifier: .getmicrosoftkey.com
    Subject Identifier: .gfx-int.ms
    Subject Identifier: gfx-int.ms
    Subject Identifier: .gfx.ms
    Subject Identifier: .healthvault-ppe.co.uk
    Subject Identifier: .healthvault-ppe.com
    Subject Identifier: healthvault-ppe.com
    Subject Identifier: .healthvault.co.uk
    Subject Identifier: .healthvault.com
    Subject Identifier: .hotmail-int.com
    Subject Identifier: hotmail.co.uk
    Subject Identifier: .hotmail.com
    Subject Identifier: hotmail.com
    Subject Identifier: iespdytst
    Subject Identifier: ieta-wa-24
    Subject Identifier: .live-int.com
    Subject Identifier: .live-int.net
    Subject Identifier: .live-partner.com
    Subject Identifier: .live-ppe.net
    Subject Identifier: .live.com
    Subject Identifier: .live.fi
    Subject Identifier: live.fi
    Subject Identifier: .live.net
    Subject Identifier: .livefilestore-int.com
    Subject Identifier: .livefilestore.com
    Subject Identifier: .livemeeting.com
    Subject Identifier: .lync.com
    Subject Identifier: .mesh.com
    Subject Identifier: .mgmt.live
    Subject Identifier: .microsoft-int.com
    Subject Identifier: .microsoft.com
    Subject Identifier: .redmond.corp.microsoft.com
    Subject Identifier: download.microsoft.com
    Subject Identifier: iespdytst.redmond.corp.microsoft.com
    Subject Identifier: microsoft.com
    Subject Identifier: powerusers-staging.microsoft.com
    Subject Identifier: powerusers.microsoft.com
    Subject Identifier: telecommand.telemetry.microsoft.com
    Subject Identifier: vortex-sandbox.data.microsoft.com
    Subject Identifier: watson.telemetry.microsoft.com
    Subject Identifier: .microsoft.com.au
    Subject Identifier: .microsoft.com.tr
    Subject Identifier: .microsoft.fr
    Subject Identifier: .microsoftonline-int.com
    Subject Identifier: .microsoftonline-p-int.com
    Subject Identifier: .microsoftonline-p.com
    Subject Identifier: .microsoftonline-p.net
    Subject Identifier: .microsoftonline.com
    Subject Identifier: .microsoftonline.net
    Subject Identifier: .microsoftprime.com
    Subject Identifier: .microsoftstore.com
    Subject Identifier: za.microsoftstore.com
    Subject Identifier: .microsoftstore.com.br
    Subject Identifier: .microsoftstore.com.cn
    Subject Identifier: .microsoftstore.com.hk
    Subject Identifier: .microsofttranslator.com
    Subject Identifier: .microsoftvirtualacademy.com
    Subject Identifier: .modern.ie
    Subject Identifier: modern.ie
    Subject Identifier: .msads.net
    Subject Identifier: .vo.msecnd.net
    Subject Identifier: .msgamestudios.com
    Subject Identifier: .msn-int.com
    Subject Identifier: .msn.cn
    Subject Identifier: .msn.co.jp
    Subject Identifier: .msn.com
    Subject Identifier: .msn.com.cn
    Subject Identifier: .msocdn.com
    Subject Identifier: .firstpartyapps.oaspapps.com
    Subject Identifier: .office-int.com
    Subject Identifier: office-int.com
    Subject Identifier: .office-int.net
    Subject Identifier: .office.com
    Subject Identifier: office.com
    Subject Identifier: .office.net
    Subject Identifier: .office365.com
    Subject Identifier: .officeppe.com
    Subject Identifier: .officeppe.net
    Subject Identifier: .onedrive.com
    Subject Identifier: onedrive.com
    Subject Identifier: .onenote.com
    Subject Identifier: onenote.com
    Subject Identifier: .onenote.net
    Subject Identifier: outlook-int.com
    Subject Identifier: .outlook.com
    Subject Identifier: 003-1-d.outlook.com
    Subject Identifier: 003-1-d.prod.outlook.com
    Subject Identifier: outlook.com
    Subject Identifier: pod71084-pri.outlook.com
    Subject Identifier: pod71084.outlook.com
    Subject Identifier: .pfx.ms
    Subject Identifier: .s-microsoft.com
    Subject Identifier: .s-msft.com
    Subject Identifier: .s-msn.com
    Subject Identifier: .sfx-df.ms
    Subject Identifier: .sfx-int.ms
    Subject Identifier: .sfx.ms
    Subject Identifier: .sharepoint.com
    Subject Identifier: .sharepointonline.com
    Subject Identifier: .skype.com
    Subject Identifier: community-stage.skype.com
    Subject Identifier: .skype.net
    Subject Identifier: .skypeassets.com
    Subject Identifier: .sqlazurelabs.com
    Subject Identifier: .surface.com
    Subject Identifier: .syncxp.net
    Subject Identifier: .trouter.io
    Subject Identifier: .virtualearth.net
    Subject Identifier: .visualstudio.com
    Subject Identifier: visualstudio.com
    Subject Identifier: .windows-int.net
    Subject Identifier: .windows.com
    Subject Identifier: insidersurveys.windows.com
    Subject Identifier: www.insidersurveys.windows.com
    Subject Identifier: .windows.net
    Subject Identifier: .windowsazure.com
    Subject Identifier: .windowsmedia.com
    Subject Identifier: .windowsphone-int.com
    Subject Identifier: .windowsphone-int.net
    Subject Identifier: .windowsphone.com
    Subject Identifier: .windowsphone.net
    Subject Identifier: .windowssearch.com
    Subject Identifier: .windowsstore.com
    Subject Identifier: .wlxrs.com
    Subject Identifier: .xbox.com
    Subject Identifier: .xboxlive.com
    Subject Identifier: .zune.net

Also, the lastsync timestamp (2016-09-24 14:22:44 UTC) shows that this list is being regularly updated. 

So this very much looks like evidence of an active system-wide certificate pinning mechanism protecting against MITM attacks on high-value Microsoft domains. Which, per se, is a good thing! Some official documentation would be nice, though.

Edit 1 (2016-09-24): This seems to be related to Windows 10 Telemetry, as briefly mentioned at this single page:  https://technet.microsoft.com/en-us/itpro/windows/manage/configure-windows-telemetry-in-your-organization 

<a href="http://twitter.com/share" class="twitter-share-button" 
data-url="https://hexatomium.github.io/2016/09/24/hidden-w10-pins/" data-text="Windows 10's Undocumented Certificate Pinning Feature"  data-count="horizontal">Tweet</a>
<script type="text/javascript" src="http://platform.twitter.com/widgets.js"></script>

<A href=https://twitter.com/hexatomium>Follow</A> @hexatomium
