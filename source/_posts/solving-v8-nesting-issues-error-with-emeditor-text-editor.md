---
title: Solving 'V8 Nesting Issues' Error with EmEditor Text Editor
date: 2024-10-09T10:36:04.278Z
updated: 2024-10-13T20:32:55.749Z
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
<li><a href="https://youtube-web.techidaily.com/024-approved-creative-vlog-ideas-for-daily-use/"><u>[New] 2024 Approved Creative Vlog Ideas for Daily Use</u></a></li>
<li><a href="https://instagram-video-recordings.techidaily.com/updated-2024-approved-building-your-influencer-empire-on-instagram-practical-5-step-guide/"><u>[Updated] 2024 Approved Building Your Influencer Empire on Instagram Practical 5-Step Guide</u></a></li>
<li><a href="https://some-techniques.techidaily.com/updated-first-step-in-film-making-best-8-cameras-35mm-to-pands/"><u>[Updated] First Step in Film Making Best 8 Cameras (35Mm to P&S)</u></a></li>
<li><a href="https://article-posts.techidaily.com/updated-in-2024-from-lenses-to-screens-reviewing-nikon-d7500/"><u>[Updated] In 2024, From Lenses to Screens Reviewing Nikon D7500</u></a></li>
<li><a href="https://phone-solutions.techidaily.com/3-solutions-to-hard-reset-vivo-v30-phone-using-pc-drfone-by-drfone-reset-android-reset-android/"><u>3 Solutions to Hard Reset Vivo V30 Phone Using PC | Dr.fone</u></a></li>
<li><a href="https://extra-information.techidaily.com/a-complete-guide-about-video-resolution-for-beginners/"><u>A Complete Guide About Video Resolution for Beginners</u></a></li>
<li><a href="https://win-lab.techidaily.com/avoid-windows-memory-buffering-in-handling-massive-files-using-emeditor-text-editor/"><u>Avoid Windows' Memory Buffering in Handling Massive Files Using EmEditor Text Editor</u></a></li>
<li><a href="https://win-lab.techidaily.com/enhance-your-writing-with-emeditor-a-comprehensive-multi-language-text-editor-solution/"><u>Enhance Your Writing with EmEditor - A Comprehensive Multi-Language Text Editor Solution</u></a></li>
<li><a href="https://change-location.techidaily.com/in-2024-can-life360-track-you-when-your-infinix-zero-5g-2023-turbo-is-off-drfone-by-drfone-virtual-android/"><u>In 2024, Can Life360 Track You When Your Infinix Zero 5G 2023 Turbo is off? | Dr.fone</u></a></li>
<li><a href="https://win-lab.techidaily.com/mastering-line-removal-with-emeditors-custom-curtext-parsing-feature/"><u>Mastering Line Removal with EmEditor's Custom CurText Parsing Feature</u></a></li>
<li><a href="https://buynow-help.techidaily.com/navigating-the-transition-from-old-to-new-macos-version/"><u>Navigating the Transition From Old to New MacOS Version</u></a></li>
<li><a href="https://win-lab.techidaily.com/professional-text-editing-with-emeditor-v10-release-candidate-powerful-unicode-support/"><u>Professional Text Editing with EmEditor v10 Release Candidate - Powerful Unicode Support</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/2135412/19272" target="_top" id="2135412">
  <img src="//a.impactradius-go.com/display-ad/19272-2135412" border="0" alt="https://techidaily.com" width="250" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/2135412/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

