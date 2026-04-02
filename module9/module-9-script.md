# Module 9 Script: Embedding Media

---

## Intro

Welcome to the final module. The Space Jam site was released in 1996, right at the moment when the web was first trying to handle audio and video. The people who built it wanted the site to feel cinematic — not just text and images but actual movie clips, interactive 360-degree panoramas, and downloadable voice clips from the Looney Tunes characters.

In this module we are building two of those media pages. The first is the Planet B-Ball QTVR viewer — a page where a QuickTime VR panorama of Michael Jordan's training facility plays inline in the browser. The second is a Looney Tunes sounds page where visitors can download character voice clips in their choice of format.

These two pages represent the two ways the Space Jam site handles media: one embeds content to play directly in the page, the other just offers files for download.

---

## The embed Tag

[Open completed/centercourt.html in a text editor. Point to the embed tag.]

The embed tag inserts a media file into the page. Where an img tag shows a still image, embed brings in something the browser hands off to a plugin — a QuickTime movie, a QuickTime VR panorama, a Shockwave game, a sound file.

The attributes look similar to what you have seen on img: src is the file path, width and height set the dimensions of the player area in pixels. Then there are plugin-specific attributes. For QuickTime, autoplay=true starts playback as soon as the file loads. The QTVR-specific attributes — pan and correction — control the initial view angle and image quality.

[Point to the embed tag in the file.]

One thing to notice: embed has no closing tag. Like br and img, it stands alone.

[Pause.]

I should be honest about something. QuickTime VR required a browser plugin that no modern browser supports. If you open this page today, the embed tag will render as an empty gray box or nothing at all. The markup is correct — the technology it depends on is just gone. We are writing it here because it is part of the original site and understanding what it did is part of understanding 1996 web development.

---

## Linking to Downloadable Files

[Open completed/sounds.html in a text editor. Point to the list items with the AIF and WAV links.]

The second kind of media delivery is much simpler: a plain link tag pointing to a file. The browser receives the file and, because it is an audio or video format it cannot display as a web page, it either opens a download dialog or hands it to an external application.

The link tag is exactly what you learned in Module 4. The only difference is the href points to an audio file instead of an HTML file. That is it. There is no special tag for file downloads in 1996 HTML.

[Point to the AIF and WAV links on one line item.]

The Space Jam site offers every audio clip in two formats: AIF for Mac users, WAV for Windows users. In 1996 these were largely separate audiences — most software existed in separate Mac and Windows editions. So the pattern on every download page is: clip name, then a link for AIF, then a link for WAV. The user picks whichever format their computer can open.

---

## Lists for Download Pages

[Point to the ul and li tags in sounds.html.]

You have seen unordered lists since Module 4. Download pages are a natural fit for them. Each li is one audio clip: the character, a description of what they say, and the format links inline after it.

This exact pattern — ul, li, clip name in bold, format links in parentheses — appears on every download page in the Space Jam site. It was a common convention across the entire web in the mid-nineties. Users knew to look for the parenthetical format links.

---

## The hr Tag

[Point to the hr tags in sounds.html.]

The hr tag draws a horizontal rule — a dividing line across the page. It has no closing tag. Two attributes worth knowing:

Width sets how wide the line is, either in pixels or as a percentage of the container. Setting it to 75% or 50% gives the line a centered, elegant look instead of stretching edge to edge.

Noshade renders the line as flat instead of embossed. The default hr has a slight 3D shadow effect from the nineties aesthetic. Noshade gives you a clean, flat line.

---

## Exercise Walkthrough: Part A — The QTVR Viewer

Let's build centercourt.html first.

**Step 1 — Page setup.**

[Create centercourt.html in the editor.]

Title it "Planet B-Ball." Now set the body attributes. This section has its own distinct color scheme, completely different from the rest of the site.

[Point to the body tag in the completed file.]

The background color is #18ad11 — a basketball-green. The background tile is bg-bball.gif. Text is a deep blue, #030762. Links are also blue. The designer wanted this section to feel like a basketball court, not outer space.

**Step 2 — The JordanDome header.**

Inside the body, add a br tag, then a centered b-jordandome.gif image — 299 wide by 93 tall. This is the title graphic for the section.

**Step 3 — The embed.**

Below the header, open a blockquote. Add an introductory line in font size +1: "If you have the latest QuickTime plug-in for your browser, you will see the QTVR below."

Then, in a center tag, add the embed tag. src points to assets/centercourt.qt — note that this file is not in the assets folder because it is large, so it will show as a placeholder. Width 320, height 200, autoplay=true. The QTVR-specific attributes are pan=100 and correction=full.

**Step 4 — Usage instructions and download links.**

Below the embed, still in the blockquote, add instructions in font size +1. Something like: "Use your mouse with the button down to move around. Control to zoom out. Option on Mac or Shift on PC to zoom in." Then add a fallback sentence offering the QTVR file as a downloadable link for users without the plugin — one link for the Mac HQX file and one for the Windows ZIP.

**Step 5 — Footer.**

Close the blockquote. Add the navigation footer using the same nobr/center pattern from earlier modules. qtvr.gif links back to qtvr.html, then the copyright notice, then next.gif links to gym.html.

[Save and open in the browser.]

The page should show the green court background, the JordanDome title, a placeholder where the QTVR would play, and the instructions below.

---

## Exercise Walkthrough: Part B — The Audio Download Page

Now let's build sounds.html.

**Step 1 — Page setup.**

[Create sounds.html in the editor.]

Title it "Space Jam - Sounds." Black body, red text, the standard Space Jam palette.

**Step 2 — Heading and first hr.**

Inside a center tag, add the page heading in font size +2: "Looney Tunes Voice Clips." Below it, an hr tag with width="75%" and noshade.

**Step 3 — The download list.**

Add a table with width="90%" and border="0" — this just constrains the list width so it does not stretch across a huge monitor. Inside the table, one row, one cell. Inside that cell, open a ul tag.

For each clip, write an li tag. Start with the character name in bold. Then an em dash. Then the clip description in quotes. Then in parentheses, the AIF link and the WAV link. End with two br tags for spacing before the next item.

[Add a couple on screen, narrating the pattern.]

Bugs Bunny — "Yeah!" — in parentheses, an a tag with href pointing to yeah.aif in assets, text "AIF." Then the WAV link if the WAV exists. Then two br tags.

Continue through all six clips in the assets folder.

Close the ul, the td, the tr, the table.

**Step 4 — Second hr and footer.**

Add a second hr with width="50%" and noshade — this one is narrower, signaling the end of the content. Below it, the copyright notice in font size -1.

[Save and open in the browser.]

You should see the heading, the dividing line, then the list of clips with AIF and WAV links. Click one of the links — your browser should either play the audio or prompt you to download it.

---

## Wrap-up

[Show both completed pages in the browser.]

These two pages demonstrate the full range of how the 1996 Space Jam site delivered media: the embed tag for inline playback of plugin-rendered content, and the humble anchor tag for file downloads.

[Step back and show the full course folder structure if possible.]

You have now covered every major HTML technique used in the Space Jam site: document structure, text and typography, colors and backgrounds, links, images, tables, image maps, frames, and media embedding. Module 10 in the outline is the final assembly — taking everything you have built and wiring it together into a complete navigable site that mirrors the original.

Congratulations on making it through. Now go build the rest of it.
