# Module 1 Script: The Skeleton

---

## Intro

Welcome to Introduction to HTML: Rebuilding the Space Jam Website.

In this course we are going to recreate the original 1996 Space Jam website from scratch — the one Warner Bros. put up to promote the movie, and the one that has somehow survived on the internet for nearly thirty years. It is a perfect learning project because it uses real HTML the way it was actually written in the nineties, and every page in it builds on the same small set of concepts we are going to cover together.

In this first module, we are not building anything fancy. We are building the skeleton — the bare minimum that every single HTML page needs to exist. By the end you will have a file that opens in a browser, shows "Space Jam" in the tab, and displays a heading on screen. That is it. But that foundation is what everything else will sit on.

Let's get into it.

---

## What is HTML?

HTML stands for HyperText Markup Language. That sounds more complicated than it is.

All it means is this: HTML is a plain text file with special instructions wrapped around the content. Those instructions are called tags, and the browser reads them to figure out what to display and how.

[Show the completed/index.html file in a text editor.]

Here you can see a finished HTML file. Notice those words wrapped in angle brackets — the less-than and greater-than signs. Those are tags. An opening tag is just the tag name inside those brackets. A closing tag is the same thing, but with a forward slash before the name. Most tags work this way — they wrap around something. Whatever sits between the opening and closing tag is the content that tag applies to.

The browser reads your file top to bottom, sees these tags, and renders the result on screen. That is the whole model. Everything else is just more tags.

One important thing: an HTML file is just a text file. There is nothing special about it until you save it with the dot-html extension. That extension is what tells the browser to treat it as a web page.

---

## The Four Required Tags

Every HTML page — from the simplest skeleton to the most complex site — contains the same four tags.

[Keep the completed/index.html file visible. Point to each tag as you describe it.]

The first is the html tag — you can see it right at the top and again at the very bottom. It wraps the entire document. It opens at the top and closes at the bottom. Everything in the file sits between these two tags, and they tell the browser: everything in here is HTML.

Inside the html tag, there are two sections. The first is the head tag. The head contains information *about* the page — things the browser needs to know, but that the user does not see on screen. Think of it as the behind-the-scenes area.

Inside the head is the title tag. Whatever text you put between the title tags is what appears in the browser tab, and in bookmarks. Right now it says "Space Jam." Open the browser and point to the tab — you can see it there. That is the only thing from the head section that the user experiences directly.

The second section inside the html tag is the body tag. Everything you can *see* on the page lives here — text, images, links, everything. If it is not in the body, it is not on screen.

Notice how the tags nest. The title is inside the head, which is inside the html tag. The body is also inside html, sitting after the head closes. This nesting structure is how all HTML works — tags contain other tags, which contain other tags, forming a hierarchy from the outside in.

---

## Comments

[Switch to showing a blank editor, or highlight the first line of the completed file.]

Before we write the file, there is one more thing worth knowing: HTML comments.

A comment is a note in your code that the browser completely ignores. It never shows up on screen. You use them to leave messages for yourself or anyone else reading the source.

[Point to the comment line at the top of the completed file.]

You can see one right here at the top of the file. Comments start with a less-than sign, an exclamation mark, and two dashes. They close with two dashes and a greater-than sign. Anything between them is invisible to the browser.

If you right-click on the real Space Jam page and view source, the very first line is a copyright notice written as a comment. We are going to include that in our version.

---

## Headings

[Point to the h1 line in the completed file.]

The last concept for this module is headings. HTML has six heading levels — h1 through h6. H1 is the largest and most important. H6 is the smallest. You use them like any other tag: opening tag, content, closing tag.

We need a heading in the body so that when we open the page there is something visible on screen. Right now it will just be big bold text on a white background. That is fine — color and images come in later modules.

---

## Exercise Walkthrough

Alright, let's build it.

[Open a plain text editor on screen — Notepad, TextEdit in plain text mode, or any code editor.]

Open a plain text editor. On Windows that is Notepad. On Mac, open TextEdit — and make sure you are in plain text mode. You can check by going to the Format menu. If it says "Make Plain Text," click that. If it already says "Make Rich Text," you are already in plain text mode and you are good.

Create a new file. We are going to save it as index.html. The name "index" is conventional for a home page — web servers look for a file with that name first when someone visits a folder.

**Step 1 — Add the document structure.**

[Type or paste the structure into the editor as you narrate each part.]

Start with the html tag — this is the outermost wrapper for the whole document. Inside it, add a head tag. Inside the head, add a title tag with "Space Jam" between them. Close the head. Then open a body tag and close it right away — we will put content in there in a moment. Finally, close the html tag.

Save the file as index.html. Now drag it into a browser window, or right-click it and choose Open With, and pick your browser.

[Show the browser with the tab visible.]

You will see a completely blank white page — but look at the tab. It says "Space Jam." The title tag is working. The head is doing its job behind the scenes.

**Step 2 — Add the comment.**

[Return to the editor.]

Go to the very first line of your file, before the html tag, and add the copyright comment. Open with a less-than, exclamation mark, two dashes. Write "Copyright 1996 Warner Bros. Online." Close with two dashes and a greater-than sign.

Save and refresh the browser.

[Show the browser refreshing.]

Nothing changes visibly — comments are invisible. But we are matching the structure of the original file.

**Step 3 — Add a heading.**

[Return to the editor. Click inside the body tags.]

Inside the body tags, add an h1 tag with "Space Jam" between the opening and closing tags.

Save and refresh.

[Show the browser.]

Now "Space Jam" appears on screen as a large heading. Plain, unstyled, black text on white — but it is there. That is your skeleton.

---

## Wrap-up

[Show the completed/index.html file side by side with what the student just built.]

Your file should look just like this. Eleven lines. And yet this is exactly what the Space Jam home page is built on — the same four tags, the same nesting structure.

In Module 2 we fill the body with real content: paragraphs, bold text, italics, line breaks, and a full character bio. In Module 3 we add the black starfield and the logo.

See you there.
