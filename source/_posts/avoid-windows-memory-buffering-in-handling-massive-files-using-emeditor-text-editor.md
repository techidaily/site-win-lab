---
title: Avoid Windows' Memory Buffering in Handling Massive Files Using EmEditor Text Editor
date: 2024-10-13T02:18:08.217Z
updated: 2024-10-14T04:24:25.926Z
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
<li><a href="https://fox-cloud.techidaily.com/new-elevating-zoom-quality-best-practices-for-google-meet-for-2024/"><u>[New] Elevating Zoom Quality Best Practices for Google Meet for 2024</u></a></li>
<li><a href="https://fox-blue.techidaily.com/new-techniques-for-gradual-audio-reduction-with-lumafusion-for-2024/"><u>[New] Techniques for Gradual Audio Reduction with Lumafusion for 2024</u></a></li>
<li><a href="https://article-helps.techidaily.com/updated-in-2024-cinema-grade-camera-lineup-the-1-to-18-selections/"><u>[Updated] In 2024, Cinema-Grade Camera Lineup - The #1 to #18 Selections</u></a></li>
<li><a href="https://extra-skills.techidaily.com/updated-mac-users-the-best-5-streaming-platforms-revealed/"><u>[Updated] Mac Users The Best 5 Streaming Platforms Revealed</u></a></li>
<li><a href="https://win-lab.techidaily.com/enhance-your-writing-with-emeditor-a-comprehensive-multi-language-text-editor-solution/"><u>Enhance Your Writing with EmEditor - A Comprehensive Multi-Language Text Editor Solution</u></a></li>
<li><a href="https://win-lab.techidaily.com/finding-and-matching-text-up-to-a-newline-or-eof-using-emeditors-features/"><u>Finding and Matching Text Up to a Newline or EOF Using EmEditor's Features</u></a></li>
<li><a href="https://win-lab.techidaily.com/how-to-fix-unavailable-issues-with-emeditors-scriptgroups-in-your-editing-sessions/"><u>How to Fix 'Unavailable' Issues with EmEditor's ScriptGroups in Your Editing Sessions</u></a></li>
<li><a href="https://facebook-video-share.techidaily.com/in-2024-visual-storyteller-toolkit/"><u>In 2024, Visual Storyteller Toolkit</u></a></li>
<li><a href="https://bypass-frp.techidaily.com/is-gsm-flasher-adb-legit-full-review-to-bypass-your-vivo-y77tfrp-lock-by-drfone-android/"><u>Is GSM Flasher ADB Legit? Full Review To Bypass Your Vivo Y77tFRP Lock</u></a></li>
<li><a href="https://win-lab.techidaily.com/mastering-line-removal-with-emeditors-custom-curtext-parsing-feature/"><u>Mastering Line Removal with EmEditor's Custom CurText Parsing Feature</u></a></li>
<li><a href="https://extra-skills.techidaily.com/pickus-claim-the-ultimate-editor-or-just-another-featured-app-in-android-in-2024/"><u>PickU's Claim – The Ultimate Editor or Just Another Featured App in Android, In 2024</u></a></li>
<li><a href="https://win-lab.techidaily.com/professional-text-editing-with-emeditor-v10-release-candidate-powerful-unicode-support/"><u>Professional Text Editing with EmEditor v10 Release Candidate - Powerful Unicode Support</u></a></li>
<li><a href="https://extra-skills.techidaily.com/simplified-rss-feed-creation-methods-for-podcasters-for-2024/"><u>Simplified RSS Feed Creation Methods for Podcasters for 2024</u></a></li>
<li><a href="https://win-lab.techidaily.com/solving-v8-nesting-issues-error-with-emeditor-text-editor/"><u>Solving 'V8 Nesting Issues' Error with EmEditor Text Editor</u></a></li>
<li><a href="https://win-lab.techidaily.com/step-by-step-comparison-of-incremental-and-full-text-search-in-emeditor/"><u>Step-by-Step Comparison of Incremental and Full Text Search in EmEditor</u></a></li>
<li><a href="https://win-lab.techidaily.com/ultimate-text-editor-discover-emeditor-your-ideal-solution/"><u>Ultimate Text Editor: Discover EmEditor - Your Ideal Solution</u></a></li>
<li><a href="https://smart-video-editing.techidaily.com/updated-mac-users-learn-how-to-download-and-install-kinemaster/"><u>Updated Mac Users Learn How to Download and Install KineMaster</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<span id="1975658">
					<video width="128" height="480" style="cursor:pointer"
           poster="//a.impactradius-go.com/display-clicktoplayimage/1975658.png"
           onclick="if(!this.playClicked){this.play();this.setAttribute('controls',true);this.playClicked=true;}">
	   <source src="//a.impactradius-go.com/display-ad/22993-1975658">
	   <img src="//a.impactradius-go.com/display-clicktoplayimage/1975658.png" style="border: none; height: 100%; width: 100%; object-fit: contain">
	</video>
	<div style="width:80px;text-align:center"><a href="javascript:window.open(decodeURIComponent('https%3A%2F%2Fhomestyler.sjv.io%2Fc%2F5597632%2F1975658%2F22993'), '_blank');void(0);">Click here</a></div>
</span>
<img height="0" width="0" src="https://imp.pxf.io/i/5597632/1975658/22993" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

