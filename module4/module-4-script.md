# Module 4 Script: Links

---

## Intro

Welcome back. So far we have built a page with structure, a page with styled text, and a page with colors and images. But none of those pages connect to anything. They just sit there.

In this module we are going to change that. We are adding links.

[Show the completed/looneybios.html, bugs.html, and daffy.html all open in separate browser tabs.]

By the end of this module you will have three pages that link to each other: a Looney Tunes bios index, the Bugs Bunny bio, and the Daffy Duck bio. You will be able to navigate between all three just like a real section of a website.

---

## The a Tag

[Open the completed/bugs.html in a text editor. Scroll to the footer where the linked images are.]

Links are made with the a tag. The "a" stands for anchor. The most important attribute on it is href — hypertext reference — which is just a fancy way of saying "the address this link goes to."

The a tag wraps around whatever you want to be clickable. Most of the time that is text. But look at this footer — the a tag is wrapping an img tag. Clicking the image navigates to the URL in the href. That is all there is to it.

[Point to the border=0 on the img inside the link.]

Notice the border equals zero on the image. Without that, browsers draw a colored border around any image that is inside a link — a rectangle that matches the link color. On the Space Jam site that would be bright cyan, which looks terrible around a navigation button. Border equals zero suppresses it. You will see this on every linked image in the entire codebase.

---

## Relative vs. Absolute Paths

[Show the bugs.html file. Point to the href values in the footer links.]

The href here says just "daffy.html" — no folder, no http, nothing else. That is a relative path. It means "look for a file called daffy.html in the same folder as this page." Since bugs.html and daffy.html are both in the same folder, that is all you need.

[Point to the malogosm link in jamcentralnav.html if visible, or describe it.]

An absolute path is different. It starts with https:// and includes the full URL. You use that when linking to a different website entirely. The Space Jam site uses absolute paths for links to Warner Bros., the Studio Store, and Mars Attacks.

For navigating between your own pages in the same folder: relative paths. For linking out to the internet: absolute paths.

You can also navigate between folders. Two dots and a slash means "go up one folder." A folder name and a slash means "go down into that folder." The nav file in the Space Jam frameset uses paths like "../behind/behindframes.html" to reach sibling sections — up one folder, then into another.

---

## The target Attribute

[Show a link that has target="_top" in the nav file.]

The target attribute controls where the linked page opens. You have already seen two values.

Target equals underscore blank opens the page in a new browser tab. The Space Jam site uses this for external links — when someone clicks out to Warner Bros. or Mars Attacks, their Space Jam tab stays open.

Target equals underscore top breaks out of any frames and loads the page in the full browser window. You will see this used throughout the site, particularly in the nav frame. When the user navigates to a new section, they need to break out of the current frameset and into the new section's frameset. Underscore top makes that happen. Frames are the subject of Module 8 — for now just know the value exists.

---

## Lists

[Open the completed/looneybios.html in a text editor.]

The bios index page uses an unordered list. The ul tag creates the list container, and each li tag is one item in it.

You can put anything inside an li — plain text, links, images. Here each item is a character's name wrapped in a link tag. The browser automatically adds bullet points and indentation.

The Space Jam site uses lists extensively for navigation and download pages. Once you have seen the pattern — ul, then a series of li items — you will recognize it everywhere.

---

## Exercise Walkthrough

Let's build the three pages.

**Step 1 — Add links to bugs.html.**

[Open the Module 2 completed bugs.html in an editor. Scroll to the footer.]

Take your bugs.html from Module 2. Find the two image tags in the footer — bios.gif and next.gif. Right now they are bare image tags. Wrap each one in an a tag.

The bios image gets an href of "looneybios.html" — that is the index page we are about to create. The next image gets an href of "daffy.html" — the next character in the lineup.

Save the file.

**Step 2 — Create daffy.html.**

[Create a new file in the editor.]

Create daffy.html in the same folder. Use the same skeleton structure from Module 1 with the title "The Lineup." Apply the same body color scheme as bugs.html — same black background and yellow text. The Lineup section uses a consistent palette across all its pages.

Inside the body, follow the same pattern as bugs.html: the centered title graphic using ct-daffy.gif, then a blockquote with the character photo c-daffy.jpg floating left, the article text, and a footer row.

In the footer, the bios image still links back to looneybios.html. The next image links to porky.html — which does not exist yet, and that is fine. Links can point to pages you have not built.

**Step 3 — Create looneybios.html.**

[Create a third file.]

Create looneybios.html. Give it the title "The Lineup" and the same black body with yellow text. Add a centered h2 heading that says "Looney Tunes Bios." Then add a blockquote with an unordered list: one li for Bugs Bunny linking to bugs.html, one li for Daffy Duck linking to daffy.html.

**Step 4 — Test the navigation.**

[Open looneybios.html in a browser.]

Open looneybios.html. You should see the two character names as clickable links. Click Bugs Bunny — you land on the bio page. The images and article text are all there. Scroll to the footer and click the next button — you arrive at Daffy Duck's page. Click the bios button — you are back at the index.

[Navigate through all three pages on screen.]

Three pages, all connected. That is how the entire Lineup section of the Space Jam site works — and it is how most of the early web worked.

---

## Wrap-up

[Show the completed/ folder files alongside the student's version.]

Compare your files to the completed folder. In Module 5 we go back to the home page and add all the section button images. In Module 6 we arrange those images properly using a table. We are getting close to the real thing.

See you there.
