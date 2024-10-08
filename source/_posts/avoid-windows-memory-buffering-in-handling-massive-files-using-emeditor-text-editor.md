---
title: Avoid Windows' Memory Buffering in Handling Massive Files Using EmEditor Text Editor
date: 2024-10-04T16:49:39.233Z
updated: 2024-10-08T16:37:46.301Z
tags:
  - product
categories:
  - emeditor
thumbnail: https://thmb.techidaily.com/0b2657385f18cc859d59520b24816f771e8e749f151532892ba053a97dc454cb.jpg
---

## Avoid Windows' Memory Buffering in Handling Massive Files Using EmEditor Text Editor

Viewing 2 posts - 1 through 2 (of 2 total)

* Author  
Posts
* February 26, 2008 at 2:33 pm [#5507](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/f1acb3fbde4e523cd2b85c48dea8bcd3?s=80&d=identicon&r=g)MattP](https://www.emeditor.com/forums/users/MattP/ "View MattP's profile")  
Member  
Out of curiosity, are you using the FILE\_FLAG\_NO\_BUFFERING flag when working with large files? This provides a significant performance boost when working with large files in a sequential manner, such as a search. Currently in my use of EmEditor Pro, I’m working with files that are 1GB or more, and I seem to notice quite a bit of disk thrashing.  
 I’ve written some software in the past that worked with files in the 4GB to 8GB range and the overall performance of the system improved dramatically by using the FILE\_FLAG\_NO\_BUFFERING flag for CreateFile. The only downside is you now have to read/write in 512 byte chunks, but the performance gain is well worth it.  
February 26, 2008 at 5:33 pm [#5508](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/a0a6377144ed3636f985d87303f65ed2?s=80&d=identicon&r=g)Yutaka Emura](https://www.emeditor.com/forums/users/yemura/ "View Yutaka Emura's profile")  
Keymaster  
> MattP wrote:  
> Out of curiosity, are you using the FILE\_FLAG\_NO\_BUFFERING flag when working with large files? This provides a significant performance boost when working with large files in a sequential manner, such as a search. Currently in my use of EmEditor Pro, I’m working with files that are 1GB or more, and I seem to notice quite a bit of disk thrashing.  
>  
> I’ve written some software in the past that worked with files in the 4GB to 8GB range and the overall performance of the system improved dramatically by using the FILE\_FLAG\_NO\_BUFFERING flag for CreateFile. The only downside is you now have to read/write in 512 byte chunks, but the performance gain is well worth it.  
 I checked the code, and FILE\_FLAG\_NO\_BUFFERING was not used. I have experimended a lot of flag combinations, but I will certainly try that again. You might want to check the Advanced tab of the Customize dialog box (Tools menu > Customize), and set or clear “Use Temporary File to Reduce Memory Usage” or change the numeric value here. I guess the hard disk thrashing you hear might come from either (1) Windows virtual memory swapping or (2) EmEditor temporary file usage. Thanks for your inputs!
* Author  
Posts

Viewing 2 posts - 1 through 2 (of 2 total)

* You must be logged in to reply to this topic.

<ins class="adsbygoogle"
     style="display:block"
     data-ad-format="autorelaxed"
     data-ad-client="ca-pub-7571918770474297"
     data-ad-slot="1223367746"></ins>

<ins class="adsbygoogle"
     style="display:block"
     data-ad-client="ca-pub-7571918770474297"
     data-ad-slot="8358498916"
     data-ad-format="auto"
     data-full-width-responsive="true"></ins>

<span class="atpl-alsoreadstyle">Also read:</span>
<div><ul>
<li><a href="https://snapchat-videos.techidaily.com/new-in-2024-how-to-dive-into-direct-messaging-and-video-chats-in-under-a-minute/"><u>[New] In 2024, How to Dive Into Direct Messaging & Video Chats in Under a Minute</u></a></li>
<li><a href="https://eaxpv-info.techidaily.com/updated-2024-approved-free-techniques-for-turning-youtube-watching-into-a-screenshot/"><u>[Updated] 2024 Approved Free Techniques for Turning YouTube Watching Into a Screenshot</u></a></li>
<li><a href="https://bypass-frp.techidaily.com/in-2024-the-complete-guide-to-google-frp-bypass-everything-you-need-to-know-by-drfone-android/"><u>In 2024, The Complete Guide to Google FRP Bypass Everything You Need to Know</u></a></li>
<li><a href="https://facebook.techidaily.com/majority-opinion-on-tech-virtual-networking-harms-society/"><u>Majority Opinion on Tech: Virtual Networking Harms Society</u></a></li>
<li><a href="https://win-lab.techidaily.com/seamless-transfer-of-documents-between-windows-and-android-devices-via-googles-quick-share-feature/"><u>Seamless Transfer of Documents Between Windows & Android Devices via Google's Quick Share Feature</u></a></li>
<li><a href="https://win-answers.techidaily.com/solutions-for-when-your-logitech-devices-arent-working-correctly-on-pcs/"><u>Solutions for When Your Logitech Devices Aren't Working Correctly on PCs</u></a></li>
<li><a href="https://youtube-docs.techidaily.com/by-step-guide-to-creating-popular-youtube-openings-for-2024/"><u>Step-by-Step Guide to Creating Popular YouTube Openings for 2024</u></a></li>
<li><a href="https://techtrends.techidaily.com/step-by-step-guide-how-to-address-wpcapdll-missing-errors/"><u>Step-by-Step Guide: How to Address Wpcap.dll Missing Errors</u></a></li>
<li><a href="https://hardware-updates.techidaily.com/toms-tech-reviews-in-depth-analysis-of-cutting-edge-equipment/"><u>Tom's Tech Reviews: In-Depth Analysis of Cutting-Edge Equipment</u></a></li>
<li><a href="https://win-lab.techidaily.com/trouble-with-your-virtual-private-network-after-latest-windows-patch-the-culprit-might-be-aprils-microsoft-update-techinsights/"><u>Trouble with Your Virtual Private Network After Latest Windows Patch? The Culprit Might Be April's Microsoft Update | TechInsights</u></a></li>
<li><a href="https://digital-screen-recording.techidaily.com/unleash-your-inner-videographer-with-these-4-methods-on-xbox-for-2024/"><u>Unleash Your Inner Videographer with These 4 Methods on Xbox for 2024</u></a></li>
<li><a href="https://win-lab.techidaily.com/unleashing-your-pcs-potential-with-microsofts-free-powertoys-fancyzones-discover-how-and-benefits/"><u>Unleashing Your PC's Potential with Microsoft's Free PowerToys FancyZones - Discover How & Benefits!</u></a></li>
<li><a href="https://win-lab.techidaily.com/unveiling-of-microsofts-windows-11-special-edition-computers-aimed-at-educational-institutions-insights-from-pc-manufacturers/"><u>Unveiling of Microsoft's Windows 11 Special Edition Computers Aimed at Educational Institutions - Insights From PC Manufacturers</u></a></li>
<li><a href="https://win-lab.techidaily.com/upcoming-change-alert-will-microsoft-charge-for-windows-11-updates-expected-prices-and-details-unveiled-zdnet-insights/"><u>Upcoming Change Alert: Will Microsoft Charge for Windows 11 Updates? Expected Prices & Details Unveiled | ZDNET Insights</u></a></li>
<li><a href="https://win-lab.techidaily.com/zdnet-investigates-the-value-of-older-iphones-for-todays-tech-savvy-users/"><u>ZDNet Investigates the Value of Older iPhones for Today's Tech-Savvy Users</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/1975836/19272" target="_top" id="1975836">
  <img src="//a.impactradius-go.com/display-ad/19272-1975836" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/1975836/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

