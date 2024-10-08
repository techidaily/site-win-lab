---
title: Solving 'V8 Nesting Issues' Error with EmEditor Text Editor
date: 2024-10-01T16:32:35.344Z
updated: 2024-10-08T16:00:10.311Z
tags:
  - product
categories:
  - emeditor
thumbnail: https://thmb.techidaily.com/22d9fd7a65c91efdcc82425d640f28a9aea80bb6b14188ff789f4577f0c290a1.jpg
---

## Solving 'V8 Nesting Issues' Error with EmEditor Text Editor

Viewing 1 post (of 1 total)

* Author  
Posts
* August 4, 2024 at 7:46 am [#29897](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/b5695857a6ecfde5db964f5b842293d1?s=80&d=identicon&r=g)Patrick C](https://www.emeditor.com/forums/users/patrick-c/ "View Patrick C's profile")  
Participant  
![V8 nesting issues occurred error message](https://www.yaroc.ch/__forum_images__/2024-08-04_EmEditor_V8_nesting_issues_occurred.png)  
![Exception number](https://www.yaroc.ch/__forum_images__/2024-08-04_EmEditor_V8_nesting_issues_occurred_pt2.png)  
Caused by a V8 macro executing a second V8 macro synchronously.  
Example code:  
```  
#language = "V8"  
#async = "off"  
editor.ExecuteMacro("runner.jsee", eeRunFile | eeMacroSyncOnly);  
```  
executes  
```  
#language = "V8"  
#async = "off"  
OutputBar.writeln("Hi there I’m runner!");  
```  
Removing the `eeMacroSyncOnly` flag does not raise an error but I\`ll end up in a race condition. My application requires the first macro to wait until the second macro ends.  
What works and doesn’t is:  
 ✔️ JScript executing JScript synchronously  
 ✔️ JScript executing V8 synchronously  
 ✔️ V8 executing JScript synchronously  
 ❌ V8 executing V8 synchronously 😞  
Question:  
 Is there an alternative way to wait for the second script to end (e.g. a semaphore)?  
Note that for my particular application #include is not an option.
* Author  
Posts

Viewing 1 post (of 1 total)

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
<li><a href="https://vp-tips.techidaily.com/new-2024-approved-comprehensive-analysis-of-top-6-hdmi-enabled-monitors/"><u>[New] 2024 Approved Comprehensive Analysis of Top 6 HDMI-Enabled Monitors</u></a></li>
<li><a href="https://article-tips.techidaily.com/updated-2024-approved-harness-natural-light-for-iphone-photography/"><u>[Updated] 2024 Approved Harness Natural Light for iPhone Photography</u></a></li>
<li><a href="https://tiktok-video-recordings.techidaily.com/2024-approved-boost-your-tiktok-impact-2023s-leading-font-generators/"><u>2024 Approved Boost Your TikTok Impact 2023'S Leading Font Generators</u></a></li>
<li><a href="https://win-lab.techidaily.com/best-4-display-sharing-applications-for-your-mi-device-a-comprehensive-guide/"><u>Best 4 Display Sharing Applications for Your Mi Device: A Comprehensive Guide</u></a></li>
<li><a href="https://vp-tips.techidaily.com/can-adobe-premiere-pro-handle-av1-format-importsexports-effectively/"><u>Can Adobe Premiere Pro Handle AV1 Format Imports/Exports Effectively?</u></a></li>
<li><a href="https://win-lab.techidaily.com/effective-solutions-for-when-apowerunlock-struggles-with-identifying-your-ios-device/"><u>Effective Solutions for When Apowerunlock Struggles with Identifying Your iOS Device</u></a></li>
<li><a href="https://win-lab.techidaily.com/effective-techniques-for-creating-seamless-looping-videos/"><u>Effective Techniques for Creating Seamless Looping Videos</u></a></li>
<li><a href="https://win-lab.techidaily.com/effortless-transformation-how-to-turn-videos-into-gif-format/"><u>Effortless Transformation: How to Turn Videos Into GIF Format</u></a></li>
<li><a href="https://win11-tips.techidaily.com/enhancing-user-experience-3-ways-to-boost-mouse-speed/"><u>Enhancing User Experience: 3 Ways to Boost Mouse Speed</u></a></li>
<li><a href="https://bypass-frp.techidaily.com/how-to-bypass-frp-on-realme-note-50-by-drfone-android/"><u>How to Bypass FRP on Realme Note 50?</u></a></li>
<li><a href="https://common-error.techidaily.com/resolved-how-to-fix-the-windows-update-error-code-0x8007001f/"><u>Resolved: How to Fix the Windows Update Error Code 0X8007001F</u></a></li>
<li><a href="https://win-lab.techidaily.com/setting-up-regular-tasks-configuring-software-for-predictable-launch-times/"><u>Setting Up Regular Tasks: Configuring Software for Predictable Launch Times</u></a></li>
<li><a href="https://win-lab.techidaily.com/simple-guide-how-to-record-your-entire-mac-screen-as-a-video/"><u>Simple Guide: How to Record Your Entire Mac Screen as a Video</u></a></li>
<li><a href="https://win-lab.techidaily.com/the-ultimate-guide-to-the-top-5-android-video-compressors/"><u>The Ultimate Guide to the Top 5 Android Video Compressors</u></a></li>
<li><a href="https://solve-help.techidaily.com/1725289416998-winx-dvd-digiarty/"><u>WinX DVD 操作指南 - Digiartyソフトウェアの完全なユーザーマニュアル</u></a></li>
<li><a href="https://fox-access.techidaily.com/your-ultimate-guide-to-top-9-platforms-for-2024/"><u>Your Ultimate Guide to Top 9 Platforms for 2024</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<a href="https://imp.i357552.net/c/5597632/977686/11832" target="_top" id="977686">
  <img src="//a.impactradius-go.com/display-ad/11832-977686" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://imp.i357552.net/i/5597632/977686/11832" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

