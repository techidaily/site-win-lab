---
title: "Ultimate Text Editor: Discover EmEditor - Your Ideal Solution"
date: 2024-10-10T22:12:40.871Z
updated: 2024-10-14T04:42:01.583Z
tags:
  - product
categories:
  - emeditor
thumbnail: https://thmb.techidaily.com/064bb5c43db4056e998dcb4f406cb778296c7343d435216b9b3443b144736cca.jpg
---

## Ultimate Text Editor: Discover EmEditor - Your Ideal Solution

July 27, 2016 at 2:17 pm [#20998](https://tools.techidaily.com/emeditor/products/) 

[![](https://secure.gravatar.com/avatar/21bf85a5da27278c7f73ff85a8eb81ab?s=80&d=identicon&r=g)LifeTimer](https://www.emeditor.com/forums/users/lifetimer/ "View LifeTimer's profile")

Participant

Ok, I will try to make my test case above even more easy then (NOTE: even though the description is a bit lengthy, the example itself is still very simple, the detailed description of it is just for maximum clarity), here:

Create a document containing the following exact contents:

```
Line with empty row after it (1)

Line NOT having an empty row after it
This line makes the above line not match the regexp

Line with empty row after it (2)

Last line
```

Now, perform a normal search in EmEditor (i.e. via the normal “Find” dialogue), using the following search term (which is a regexp that matches all lines that have an empty line right after them):

`^.*\n\n`

(leave all checkboxes non-checked in the Find dialogue, except the “Use Regular Expressions” checkbox, and also leave all checkboxes non-checked in the “Advanced…” sub-dialogue of the Find dialogue, as is default.

Now execute the search (i.e. press “Find next”).

You will now see, that just as expected, the following three lines match the search (i.e. they will be highlighted one at a time when you press the “Find next” button):

`Line with empty row after it (1)`

`This line makes the above line not match the regexp`

`Line with empty row after it (2)`

So far so good!

Now, filter away the line “_This line makes the above line not match the regexp_“, by using the following filter expression in EmEditor (i.e. in the Filter box in the toolbar):

`This line makes the above line not match the regexp`

The remaining displayed contents of the document after this will now be as follows:

```
Line with empty row after it (1)

Line NOT having an empty row after it

Line with empty row after it (2)

Last line
```

As you see, the line containing the string “_Line NOT having an empty row after it_” does now indeed HAVE an empty line after it, which makes the stage set for our last step, showing the bug / unexpected behavior:

Now perform the exact same search in the document as above again.

Contrary to expectation and correct regexp behavior, only the exact same lines matching the first search will match this second search, even though the line containing “_Line NOT having an empty row after it_” should now also match the search (again, because it now HAS an empty line after it).

As a programmer, I understand the problem. You run the regular expression on the entire contents of the original document, even though some of its lines are filtered out from view, and then only display the search matches that are located in lines that are not filtered out of view. BUT, this obviously doesn’t work with regular expression searches involving linebreaks (as in my example above).

This means that for this to work correctly, you must either allocate a contiguous buffer containing the contents of the current filtered data, to perform regexp searches on (which will of course involve both a memory and a CPU hit for really large files), or make a restriction (or at least clear and visible warning) that regexp searches whose hits (or lookaheads/lookbehinds) involve more than one row cannot be used at all if the contents of the current document are filtered.

Personally, I would prefer a compromise that makes such regexp searches of filtered data possible for documents that just aren’t really big (say, more than a couple of hundred megabytes or so?), and restrict it only for documents larger than that. (and I would also do the same thing for the green markings of multi-row hits by the way, since the memory usage for an extra flag per row as you mention will only be a problem at all for really big documents there too, which are, after all, not nearly as common as much smaller documents).

I hope this was clear enough to understand the issue/problem?

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
<li><a href="https://visual-screen-recording.techidaily.com/new-2024-approved-unmatched-virtual-speedway-showdowns-top-5-list/"><u>[New] 2024 Approved Unmatched Virtual Speedway Showdowns Top 5 List</u></a></li>
<li><a href="https://screen-sharing-recording.techidaily.com/new-free-guide-to-navigating-and-hosting-google-meet-sessions-effectively/"><u>[New] Free Guide to Navigating and Hosting Google Meet Sessions Effectively</u></a></li>
<li><a href="https://extra-approaches.techidaily.com/new-music-making-magic-selecting-background-beats-for-vids/"><u>[New] Music Making Magic Selecting Background Beats for Vids</u></a></li>
<li><a href="https://fox-http.techidaily.com/new-step-by-step-how-to-convert-and-download-vids-from-social-media-to-mp3s/"><u>[New] Step-by-Step How to Convert and Download Vids From Social Media to MP3s</u></a></li>
<li><a href="https://fox-cloud.techidaily.com/updated-2024-approved-uncover-the-best-5-ios-applications-for-easy-podcasting/"><u>[Updated] 2024 Approved Uncover the Best 5 iOS Applications for Easy Podcasting</u></a></li>
<li><a href="https://extra-guidance.techidaily.com/2024-approved-mastering-the-art-of-professional-gopro-cinematography/"><u>2024 Approved Mastering the Art of Professional Gopro Cinematography</u></a></li>
<li><a href="https://win-lab.techidaily.com/avoid-windows-memory-buffering-in-handling-massive-files-using-emeditor-text-editor/"><u>Avoid Windows' Memory Buffering in Handling Massive Files Using EmEditor Text Editor</u></a></li>
<li><a href="https://win-lab.techidaily.com/enhance-your-writing-with-emeditor-a-comprehensive-multi-language-text-editor-solution/"><u>Enhance Your Writing with EmEditor - A Comprehensive Multi-Language Text Editor Solution</u></a></li>
<li><a href="https://win-lab.techidaily.com/enhanced-text-manipulation-made-simple-using-emeditors-advanced-functionality/"><u>Enhanced Text Manipulation Made Simple Using EmEditor's Advanced Functionality</u></a></li>
<li><a href="https://win-lab.techidaily.com/finding-and-matching-text-up-to-a-newline-or-eof-using-emeditors-features/"><u>Finding and Matching Text Up to a Newline or EOF Using EmEditor's Features</u></a></li>
<li><a href="https://win-lab.techidaily.com/how-to-fix-unavailable-issues-with-emeditors-scriptgroups-in-your-editing-sessions/"><u>How to Fix 'Unavailable' Issues with EmEditor's ScriptGroups in Your Editing Sessions</u></a></li>
<li><a href="https://android-transfer.techidaily.com/in-2024-how-to-transfer-contacts-from-honor-90-to-outlook-drfone-by-drfone-transfer-from-android-transfer-from-android/"><u>In 2024, How to Transfer Contacts from Honor 90 to Outlook | Dr.fone</u></a></li>
<li><a href="https://digital-screen-recording.techidaily.com/in-2024-road-warriors-top-virtual-races-listed/"><u>In 2024, Road Warriors Top Virtual Races Listed</u></a></li>
<li><a href="https://win-howtos.techidaily.com/instructions-for-opting-out-of-touchscreen-functionality-in-windows-10-when-using-a-mouse-connection/"><u>Instructions for Opting Out of Touchscreen Functionality in Windows 10 when Using a Mouse Connection</u></a></li>
<li><a href="https://win-lab.techidaily.com/professional-text-editing-with-emeditor-v10-release-candidate-powerful-unicode-support/"><u>Professional Text Editing with EmEditor v10 Release Candidate - Powerful Unicode Support</u></a></li>
<li><a href="https://fix-guide.techidaily.com/reliable-user-guide-to-fix-oneplus-open-running-slow-and-freezing-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>Reliable User Guide to Fix OnePlus Open Running Slow and Freezing | Dr.fone</u></a></li>
<li><a href="https://win-lab.techidaily.com/setting-up-emeditor-v25-beta-overcoming-antivirus-issues-during-configuration/"><u>Setting up EmEditor v25 Beta - Overcoming Antivirus Issues During Configuration</u></a></li>
<li><a href="https://win-lab.techidaily.com/solving-v8-nesting-issues-error-with-emeditor-text-editor/"><u>Solving 'V8 Nesting Issues' Error with EmEditor Text Editor</u></a></li>
<li><a href="https://win-lab.techidaily.com/step-by-step-comparison-of-incremental-and-full-text-search-in-emeditor/"><u>Step-by-Step Comparison of Incremental and Full Text Search in EmEditor</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2043856/7443" target="_top" id="2043856">
  <img src="//a.impactradius-go.com/display-ad/7443-2043856" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2043856/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

