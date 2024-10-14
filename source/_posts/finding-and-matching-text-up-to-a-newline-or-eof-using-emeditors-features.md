---
title: Finding and Matching Text Up to a Newline or EOF Using EmEditor's Features
date: 2024-10-06T17:07:14.793Z
updated: 2024-10-13T17:33:55.341Z
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
<li><a href="https://remote-screen-capture.techidaily.com/new-advanced-filming-techniques-for-your-live-streaming-needs-using-logitech-cam-for-2024/"><u>[New] Advanced Filming Techniques for Your Live-Streaming Needs Using Logitech Cam for 2024</u></a></li>
<li><a href="https://article-knowledge.techidaily.com/updated-minimal-effort-maximum-recovery-for-deleted-posts/"><u>[Updated] Minimal Effort, Maximum Recovery for Deleted Posts</u></a></li>
<li><a href="https://fox-boxes.techidaily.com/updated-picsart-guide-discreetly-mask-faces/"><u>[Updated] Picsart Guide Discreetly Mask Faces</u></a></li>
<li><a href="https://digital-screen-recording.techidaily.com/updated-the-essential-audacity-manual-for-mac-audio-capture-for-2024/"><u>[Updated] The Essential Audacity Manual for Mac Audio Capture for 2024</u></a></li>
<li><a href="https://win-lab.techidaily.com/enhanced-text-manipulation-made-simple-using-emeditors-advanced-functionality/"><u>Enhanced Text Manipulation Made Simple Using EmEditor's Advanced Functionality</u></a></li>
<li><a href="https://win-lab.techidaily.com/how-to-fix-unavailable-issues-with-emeditors-scriptgroups-in-your-editing-sessions/"><u>How to Fix 'Unavailable' Issues with EmEditor's ScriptGroups in Your Editing Sessions</u></a></li>
<li><a href="https://ai-video-translation.techidaily.com/in-2024-srt-subtitle-translation-tools-and-techniques/"><u>In 2024, SRT Subtitle Translation Tools and Techniques</u></a></li>
<li><a href="https://tech-hub.techidaily.com/maximize-gpt-capabilities-with-these-9-must-try-plugins/"><u>Maximize GPT Capabilities with These 9 Must-Try Plugins</u></a></li>
<li><a href="https://win-lab.techidaily.com/setting-up-emeditor-v25-beta-overcoming-antivirus-issues-during-configuration/"><u>Setting up EmEditor v25 Beta - Overcoming Antivirus Issues During Configuration</u></a></li>
<li><a href="https://win-lab.techidaily.com/ultimate-text-editor-discover-emeditor-your-ideal-solution/"><u>Ultimate Text Editor: Discover EmEditor - Your Ideal Solution</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<a href="https://review-au.sjv.io/c/5597632/2135315/14409" target="_top" id="2135315">
  <img src="//a.impactradius-go.com/display-ad/14409-2135315" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://review-au.sjv.io/i/5597632/2135315/14409" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

