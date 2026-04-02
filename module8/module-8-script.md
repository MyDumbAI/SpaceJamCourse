# Module 8 Script: Frames

---

## Intro

Welcome back. Every section of the Space Jam site has the same structural pattern when you open it: a narrow column of navigation icons on the left side, and the section content filling the rest of the window on the right. As you click through content pages on the right, the left column stays completely still — it never reloads or changes.

[Open fullsite/cmp/jamcentral/jamcentralframes.html in a browser. Click a few nav buttons to demonstrate the persistent left column while the right side changes.]

That persistent navigation is achieved with frames. The browser window is divided into two panes, each showing a separate HTML file. The left pane always shows the same nav file. The right pane loads different content as you navigate.

In this module we are building the Jam Central frameset. By the end you will have three files: the frameset that divides the window, the nav file that fills the left column, and the Jam Central hub from Module 7 as the initial content on the right.

---

## What are Frames?

A frames page is different from a regular HTML page in one fundamental way: it has no body tag. Instead, it has a frameset tag. The frameset defines how the window is divided, and each frame inside it points to an HTML file to display in that region.

The frames are independent — each one has its own scroll position, its own navigation history, and loads its own file. The user sees what looks like one page, but the browser is actually managing two separate documents side by side.

[Pause.]

I should mention: frames are not used in modern web development. They were removed from the HTML standard years ago. We are implementing them here because the Space Jam site is built on them, and understanding them is part of understanding the site. Modern sites achieve the same persistent navigation effect with JavaScript and CSS. But in 1996, frames were the tool.

---

## frameset and frame

[Open the completed/jamcentralframes.html in a text editor.]

Look at this file. There is a head section with a title, and then instead of body, there is a frameset tag.

The frameset here uses the cols attribute set to "100,*". That means: divide the window into two columns. The first column is 100 pixels wide. The asterisk means the second column takes all the remaining space. So the left nav column is a fixed 100 pixels, and the content area fills everything else, no matter how wide the window is.

[Point to each frame tag.]

Inside the frameset are two frame tags. The first one has name="nav" and src pointing to the nav HTML file. The second has name="main" and src pointing to jamcentral.html — the content from Module 7.

---

## frame Attributes

Let's look at what each attribute on a frame tag does.

Name gives the frame an identifier. This is how links in one frame can target and load pages into another frame. We will come back to this.

Src is the HTML file to load. Same concept as the src on an img tag — a file path.

Scrolling controls whether the frame has a scrollbar. "Auto" shows a scrollbar only when the content is taller than the frame. "No" forces no scrollbar. "Yes" always shows one. The nav frame here uses auto so it can scroll if the list of buttons is taller than the window.

Noresize prevents the user from dragging the border between frames to resize them. Without this attribute, users can grab the dividing line and drag it, which can break the layout.

Marginwidth and marginheight set how much empty space surrounds the content inside a frame, in pixels. Both are set to zero here so the nav buttons and content sit flush against the frame edges.

---

## Targeting Frames with Links

[Open completed/jamcentralnav.html in a text editor.]

Here is the nav file. Every link in it has target="main". That is the name we gave the content frame.

When a user clicks a nav button, the browser loads that page into the frame named "main" — the right side — while the left nav frame stays completely untouched. That is the key mechanism.

[Point to a link in the nav file.]

The href is the content page. The target is the name of the frame to load it into. That is all there is to it.

Two special target values also appear in the Space Jam site. Target equals underscore top loads the page into the full browser window, breaking out of all frames. You use this when navigating to a completely different section that has its own frameset. Target equals underscore blank opens in a new tab — used for external links.

---

## noframes

[Point to the noframes block in jamcentralframes.html.]

The noframes tag provides fallback content. If someone opens this page in a browser that does not support frames — or has frames disabled — the frameset is ignored and the browser shows whatever is inside the noframes block instead.

Inside noframes there is a body tag with a message and a link to the non-frames version of the page. This is the safety net.

---

## Exercise Walkthrough

We are building three files. Let's go through each one.

**Step 1 — The frameset file: jamcentralframes.html.**

[Create the file in the editor.]

Create jamcentralframes.html. Write the html and head tags. Give it the title "Jam Central." Close the head.

Now — no body tag. Open a frameset tag with cols="100,*".

Inside the frameset, before the frame tags, add a noframes block. Inside noframes, write a body tag with the black starfield color scheme. Put a short message: "Your browser does not support frames. Please" followed by a link tag pointing to jamcentral.html saying "click here." Close the body and noframes.

After the noframes, add the two frame tags. First frame: name="nav", src="jamcentralnav.html", marginwidth=0, marginheight=0, scrolling="auto", noresize. Second frame: name="main", src="jamcentral.html", marginwidth=0, marginheight=0, scrolling="auto", noresize.

Close the frameset and the html tag.

**Step 2 — The nav file: jamcentralnav.html.**

[Create a second file.]

Create jamcentralnav.html. Standard html skeleton. Title "Planetary Navigation." Body with black background, bg_stars.gif tile, and white text.

Inside the body, a center tag. Then a br. Now add each nav button as an img tag wrapped in an a tag. The href points to the section's main page. The target is "main" — so it loads in the right frame. After each image, a br tag and two more br tags for spacing.

[Add the buttons, narrating a few.]

The first one: a tag with href="jamcentral.html" and target="main", wrapping the pn-jamcentralanim.gif image — height 49, width 70, alt "jam central", border=0. Close the a tag. Line break, two more line breaks.

Continue through all the nav images. The assets folder has all of them. Heights vary per image — the dimensions are listed in the lesson file. Use target="_blank" for the Mars Attacks external link at the very bottom instead of target="main".

Close center, close body, close html.

**Step 3 — The content file.**

Copy your jamcentral.html from Module 7 into the same folder. No changes needed. It will load as the initial content of the main frame.

**Step 4 — Open and test.**

[Open jamcentralframes.html in a browser.]

Open jamcentralframes.html. You should see the 100-pixel nav column on the left with the section buttons stacked vertically, and the Jam Central hub filling the right side.

Hover over the image map on the right — the four hotspots still work inside the frame. Click a nav button — the linked page will attempt to load in the right frame.

---

## Wrap-up

[Show the completed files in the browser next to the original fullsite frameset.]

Your version should look and behave like this. The same pattern — nav frame on the left, content frame on the right — is replicated across every section of the Space Jam site. Once you understand one frameset, you understand all of them.

In Module 9, the final module, we cover embedded media. See you there.
