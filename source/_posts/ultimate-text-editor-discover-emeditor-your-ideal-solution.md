---
title: "Ultimate Text Editor: Discover EmEditor - Your Ideal Solution"
date: 2024-10-05T16:53:01.037Z
updated: 2024-10-08T16:32:14.543Z
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
<li><a href="https://youtube-docs.techidaily.com/024-approved-leverage-online-platform-features-to-spread-your-music/"><u>[New] 2024 Approved Leverage Online Platform Features to Spread Your Music</u></a></li>
<li><a href="https://fox-info.techidaily.com/new-2024-approved-navigating-speed-settings-for-snapchat-content/"><u>[New] 2024 Approved Navigating Speed Settings for Snapchat Content</u></a></li>
<li><a href="https://some-techniques.techidaily.com/new-identifying-the-best-cloud-service-allies-of-2024/"><u>[New] Identifying the Best Cloud Service Allies of 2024</u></a></li>
<li><a href="https://blog-min.techidaily.com/how-to-recover-deleted-photos-from-android-gallery-app-on-magic-5-pro-by-stellar-photo-recovery-android-mobile-photo-recover/"><u>How to Recover Deleted Photos from Android Gallery App on Magic 5 Pro</u></a></li>
<li><a href="https://android-location-track.techidaily.com/in-2024-top-5-car-locator-apps-for-samsung-galaxy-xcover-7-drfone-by-drfone-virtual-android/"><u>In 2024, Top 5 Car Locator Apps for Samsung Galaxy XCover 7 | Dr.fone</u></a></li>
<li><a href="https://win-lab.techidaily.com/insiders-perspective-on-the-downside-of-working-for-microsoft-as-revealed-to-zdnet/"><u>Insider's Perspective on the Downside of Working for Microsoft, as Revealed to ZDNet</u></a></li>
<li><a href="https://win-lab.techidaily.com/microsoft-encourages-innovation-in-excel-my-response-and-experience-detailed-on-zdnet/"><u>Microsoft Encourages Innovation in Excel: My Response and Experience Detailed on ZDNet</u></a></li>
<li><a href="https://win-lab.techidaily.com/prominent-ai-experts-encourage-localized-data-framework-usage-to-enhance-diverse-representation-zdnet/"><u>Prominent AI Experts Encourage Localized Data Framework Usage to Enhance Diverse Representation | ZDNET</u></a></li>
<li><a href="https://win-lab.techidaily.com/revolutionizing-legal-workflow-microsoft-copilot-joins-forces-with-singapores-digital-law-platform-zdnet-insights/"><u>Revolutionizing Legal Workflow: Microsoft Copilot Joins Forces with Singapore's Digital Law Platform | ZDNet Insights</u></a></li>
<li><a href="https://win-lab.techidaily.com/top-rated-2023-surface-computers-in-depth-analysis-and-comparison-by-tech-experts-zdnet/"><u>Top-Rated 2023 Surface Computers: In-Depth Analysis & Comparison by Tech Experts - ZDNet</u></a></li>
<li><a href="https://smart-video-editing.techidaily.com/updated-in-2024-cool-video-editor-how-to-add-cool-effects-to-video/"><u>Updated In 2024, Cool Video Editor How to Add Cool Effects to Video</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<a href="https://ephamedtechinc.pxf.io/c/5597632/2126492/26400" target="_top" id="2126492">
  <img src="//a.impactradius-go.com/display-ad/26400-2126492" border="0" alt="https://techidaily.com" width="640" height="90"/>
</a>
<img height="0" width="0" src="https://ephamedtechinc.pxf.io/i/5597632/2126492/26400" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

