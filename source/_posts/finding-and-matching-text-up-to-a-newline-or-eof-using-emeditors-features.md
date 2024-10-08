---
title: Finding and Matching Text Up to a Newline or EOF Using EmEditor's Features
date: 2024-10-06T16:30:44.365Z
updated: 2024-10-08T16:59:17.580Z
tags:
  - product
categories:
  - emeditor
thumbnail: https://thmb.techidaily.com/aca28fbc907b3b2134a063785955f99d7ee87845f83996484c29a6f763ca253a.jpg
---

## Finding and Matching Text Up to a Newline or EOF Using EmEditor's Features

Viewing 5 posts - 1 through 5 (of 5 total)

* Author  
Posts
* July 14, 2011 at 12:08 am [#9467](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/c962eeb8483fd8ad7d82a003f8405439?s=80&d=identicon&r=g)Deipotent](https://www.emeditor.com/forums/users/deipotent/ "View Deipotent's profile")  
Participant  
I know you can use n to match a newline, but how do you match either newline OR EOF ?  
 I want it to match all lines, including the last line, which have some specific text followed by either newline or EOF. For example, I can use “sometextn”, but this won’t match on the last line.  
July 14, 2011 at 1:23 am [#9469](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/c095e276d7d1f5ed27f91bf623e4e445?s=80&d=identicon&r=g)CrashNBurn](https://www.emeditor.com/forums/users/CrashNBurn/ "View CrashNBurn's profile")  
Member  
Search for: **sometext$**  
July 14, 2011 at 2:37 am [#9475](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/c962eeb8483fd8ad7d82a003f8405439?s=80&d=identicon&r=g)Deipotent](https://www.emeditor.com/forums/users/deipotent/ "View Deipotent's profile")  
Participant  
I didn’t mention it in my original post, but I want to replace the newline, where present. For example, suppose I have three lines:  
    
	line1  
	line2  
	line3  
	 There is a newline character after “line1” and “line2”, but not after “line3”. I want to use a Find/Replace regex to convert it into the following:  
line1A, line2A, line3A  
 My Find regex would be something like  
([[:alnum:]]+)n  
 and the Replace regex would be  
1A,  
 but this does not produce want I’m after due to it not matching the last line, so the end result is:  
line1A, line2A, line3  
 That is, no “A, ” after “line3”.  
 So, I was hoping for a way to match either a n or EOF, and replace the n, but not the EOF (as that’s obviously just a virtual char).  
July 14, 2011 at 2:51 am [#9478](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/c095e276d7d1f5ed27f91bf623e4e445?s=80&d=identicon&r=g)CrashNBurn](https://www.emeditor.com/forums/users/CrashNBurn/ "View CrashNBurn's profile")  
Member  
I can’t reproduce what you are claiming in this case.  
 I’ve tried with both unix-LF and windows-CRLF files.  
AString  
	ANotherString  
	YetAnotherString  
	EvenMoreString  
 This Search: (\[\[:alnum:\]\]+)n  
 Replace: 1,  
 Results in:  
> AString, ANotherString, YetAnotherString, EvenMoreString  
July 14, 2011 at 2:58 am [#9479](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/c962eeb8483fd8ad7d82a003f8405439?s=80&d=identicon&r=g)Deipotent](https://www.emeditor.com/forums/users/deipotent/ "View Deipotent's profile")  
Participant  
Thanks CrashNBurn! The last regex is what I’m after  
([[:alnum:]]+)($n|$)
* Author  
Posts

Viewing 5 posts - 1 through 5 (of 5 total)

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
<li><a href="https://win-lab.techidaily.com/1-mastering-the-art-of-email-signatures-a-step-by-step-guide-with-microsoft-outlook/"><u>1. Mastering the Art of Email Signatures: A Step-by-Step Guide with Microsoft Outlook</u></a></li>
<li><a href="https://tech-revival.techidaily.com/access-the-most-recent-wi-fi-adapter-drivers-supporting-windows-download-for-win11-win10-win8-and-win7/"><u>Access the Most Recent Wi-Fi Adapter Drivers Supporting Windows: Download for Win11, Win10, Win8 & Win7</u></a></li>
<li><a href="https://solve-popular.techidaily.com/ameliorer-les-resultats-de-la-robotique-de-processus-assistee-par-ordinateur-rpa-analyse-et-techniques-avancees-chez-abbyy/"><u>Améliorer Les Résultats De La Robotique De Processus Assistée Par Ordinateur (RPA) - Analyse Et Techniques Avancées Chez ABBYY</u></a></li>
<li><a href="https://win-lab.techidaily.com/boost-your-surface-pros-storage-capacity-and-slash-costs-in-just-7-steps-learn-how-smarttechguru/"><u>Boost Your Surface Pro's Storage Capacity and Slash Costs in Just 7 Steps! Learn How | SmartTechGuru</u></a></li>
<li><a href="https://win-lab.techidaily.com/business-focused-chatgpt-launched-by-openai-innovative-capabilities-detailed-on-zdnet/"><u>Business-Focused ChatGPT Launched by OpenAI; Innovative Capabilities Detailed on ZDNET</u></a></li>
<li><a href="https://win-lab.techidaily.com/dont-rush-into-windows-11-top-tips-for-optimizing-your-system-without-upgrading-zdnet/"><u>Don't Rush Into Windows 11: Top Tips for Optimizing Your System Without Upgrading | ZDNet</u></a></li>
<li><a href="https://win-lab.techidaily.com/exploring-latest-innovations-in-ai-my-complete-review-of-new-copilotplus-pc-enhancements-am-i-convinced/"><u>Exploring Latest Innovations in AI: My Complete Review of New Copilot+ PC Enhancements - Am I Convinced?</u></a></li>
<li><a href="https://extra-lessons.techidaily.com/from-tweeted-videos-to-downloadable-mp3-files/"><u>From Tweeted Videos to Downloadable MP3 Files</u></a></li>
<li><a href="https://win-lab.techidaily.com/get-your-hands-on-a-steal-with-microsoft-office-2019-for-windowsmac-secure-it-now-for-just-25-expert-tips-from-zdnet/"><u>Get Your Hands on a Steal with Microsoft Office 2019 for Windows/Mac - Secure It Now for Just $25 | Expert Tips From ZDNET</u></a></li>
<li><a href="https://win-lab.techidaily.com/google-staffer-advocates-why-macos-beats-windows-on-laptops-insights-from-an-apple-enthusiast-zdnet/"><u>Google Staffer Advocates: Why macOS Beats Windows on Laptops – Insights From an Apple Enthusiast | ZDNet</u></a></li>
<li><a href="https://win-lab.techidaily.com/how-the-new-m1-pro-transforms-the-macbook-pro-into-an-unbeatable-windows-11-machine-zdnet/"><u>How the New M1 Pro Transforms the MacBook Pro Into an Unbeatable Windows 11 Machine | ZDNet</u></a></li>
<li><a href="https://techidaily.com/how-to-factory-reset-samsung-galaxy-f54-5g-without-losing-data-drfone-by-drfone-reset-android-reset-android/"><u>How to Factory Reset Samsung Galaxy F54 5G without Losing Data | Dr.fone</u></a></li>
<li><a href="https://tech-recovery.techidaily.com/how-to-overcome-display-recognition-hurdles-on-your-mac-machine/"><u>How To Overcome Display Recognition Hurdles on Your Mac Machine</u></a></li>
<li><a href="https://smart-video-editing.techidaily.com/new-minitool-movie-maker-review-guideline-and-alternatives-for-2024/"><u>New Minitool Movie Maker Review, Guideline and Alternatives for 2024</u></a></li>
<li><a href="https://facebook-video-share.techidaily.com/skyrocketing-views-live-stream-techniques-for-gamers-for-2024/"><u>Skyrocketing Views Live Stream Techniques for Gamers for 2024</u></a></li>
<li><a href="https://win11-tips.techidaily.com/taming-downloads-problems-in-win11-pc-environments-2/"><u>Taming Downloads Problems in Win11 PC Environments (2)</u></a></li>
<li><a href="https://solve-news.techidaily.com/understanding-every-dvd-format-a-comprehensive-guide/"><u>Understanding Every DVD Format: A Comprehensive Guide</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2144287/7443" target="_top" id="2144287">
  <img src="//a.impactradius-go.com/display-ad/7443-2144287" border="0" alt="https://techidaily.com" width="600" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2144287/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

