# Module 2 Script: Text & Typography

---

## Intro

Welcome back. In Module 1 we built the skeleton — the four tags that every HTML page needs. Now we are going to fill that skeleton with real content.

In this module we are building the Bugs Bunny character bio page from the Lineup section of the Space Jam site. It is a long article page, and it is a great exercise because it uses almost every text-related tag HTML has: paragraphs, bold, italic, centered content, line breaks, indented blocks, and a navigation footer at the bottom.

[Show the completed/bugs.html file rendered in a browser.]

This is where we are headed. By the end of this module you will have this page — real content, real structure. It will not have any color yet. Color comes in Module 3. But the entire layout and typography of this page will be done.

Let's go through the concepts first, then build it.

---

## Paragraphs and Line Breaks

[Open the completed/bugs.html file in a text editor. Scroll to find a paragraph ending in a `<p>` tag.]

The two most basic ways to control where text breaks in HTML are the p tag and the br tag.

The p tag creates a paragraph. The browser automatically adds space above and below it, so paragraphs are visually separated from each other. You can see in this file that each paragraph ends with a p tag. The original Space Jam site — like a lot of nineties HTML — uses p as a closing break at the end of a paragraph rather than wrapping the text inside opening and closing p tags. We are going to follow that pattern to stay true to the original.

[Point to a br tag in the file, or show a place where multiple br tags appear together.]

The br tag is different. It inserts a single line break — the cursor moves to the next line, but there is no extra space above or below. Use it when you want a new line but not a new paragraph. Notice that br has no closing tag. It just sits on its own. You will see several br tags in a row in this file, used to add vertical space between sections.

---

## Bold and Italic

[Scroll to a line in the bio where "Space Jam" appears in bold italic — something like the second paragraph.]

The b tag makes text bold. The i tag makes text italic. You can see both of them here where the movie title "Space Jam" appears in the bio. It is wrapped in a b tag on the outside and an i tag on the inside — so it gets both styles at once.

When you nest tags like this, you close them in reverse order. The last tag you opened gets closed first. So the i closes before the b. If you close them in the wrong order some browsers will still render it correctly, but it is good practice to nest them properly.

[Point to a line where just b is used, like a sub-heading within the article.]

You can also see b used on its own for the section sub-headings within the article — bold but not italic.

---

## Centering Content

[Scroll to the top of the body where the title image is wrapped in center tags.]

The center tag centers everything inside it horizontally on the page. Whatever you put inside it — text, images, other tags — gets pushed to the middle.

[Point to the center tags around the footer area too.]

You will see center used in two places in this file: at the top wrapping the title graphic, and at the bottom wrapping the navigation footer. It is one of the most common patterns in the Space Jam site. Almost every section uses it for both the header and footer areas.

---

## The font Tag

[Scroll to the footer where the font tag appears around the copyright text.]

The font tag changes the appearance of text. It has three attributes worth knowing.

The first is size. You can see it here set to negative one — written as a quoted minus one. That means "one step smaller than the browser's default text size." It is a relative value. You can also use positive numbers for larger text, or absolute numbers from one to seven. Negative one is the most common in the Space Jam site, used anywhere the original designers wanted small print.

The second attribute is color. You can see it set to a white hex code here — that is the hash followed by six f's. On a dark background, white text for the copyright notice makes sense. We will talk more about hex codes in Module 3.

The third attribute is face, which sets the font family. The Space Jam site does not use it much, but it works the same way — you give it a font name and the browser tries to use it if that font is installed.

---

## nobr

[Scroll to the footer line and show the nobr tags wrapping the whole footer content.]

The nobr tag stands for "no break." It tells the browser: do not wrap this content onto multiple lines, no matter how narrow the window is. Everything inside stays on one line.

[Resize the browser window to demonstrate, if possible, or describe the effect.]

The footer of this page has two navigation buttons and a copyright notice between them. Without nobr, if the window is narrow, those elements could split across lines and look broken. With nobr, they always stay together on a single row.

---

## blockquote

[Scroll to show the blockquote tag wrapping the main article body.]

The blockquote tag indents its content from both the left and right margins. It was originally meant for quoting a long passage from another source, but in the nineties it was also used as a simple way to give body text some breathing room from the edges of the window.

[Show the browser view of the completed page and point to the indented text.]

You can see the effect here — the article text is inset from both sides, which makes it much more readable than if it ran right to the edges of the window. The entire Bugs Bunny article is wrapped in a single blockquote.

---

## HTML Entities

[Find a line in the bio text that contains the ampersand entity — the screenwriter credits line.]

Some characters cannot be typed directly into HTML because they have special meaning. The ampersand, for example, is used to start entity codes — so if you just type an ampersand in your text, the browser gets confused and may not render it correctly.

[Point to the `&amp;` in that line.]

The solution is an entity. Entities start with an ampersand, have a short code name, and end with a semicolon. This one — ampersand, a-m-p, semicolon — produces a literal ampersand character on screen.

[Scroll to the footer where &copy; appears.]

This one — ampersand, c-o-p-y, semicolon — produces the copyright symbol. You will see it in the footer of every page in the Space Jam site.

---

## Assets

[Open the assets/ folder for this module in a file browser.]

Before we build, take a look at the assets folder. There are four files.

The ct-bugs.gif is the "Bugs Bunny" title graphic — a stylized text image that appears at the top of the page. The c-bugs.jpg is a character photo of Bugs that floats on the left side of the article. The bios.gif is a navigation button that links back to the full character list. And next.gif is a button that goes to the next character in the lineup.

You will be writing img tags that reference these files. In this module we are not going deep on how the img tag works — that is Module 5. For now, just use the attributes as shown. If you open the page and the images appear, great. If they show as broken icons, the text structure is still what matters here.

---

## Exercise Walkthrough

Let's build the page. Create a new file and save it as bugs.html.

**Step 1 — Start from the skeleton.**

[Show the completed/index.html from Module 1 for reference, then switch back to the new empty file.]

Paste in the Module 1 skeleton and change the title from "Space Jam" to "The Lineup." That is the title the original Bugs bio page uses.

**Step 2 — Add the title image and open the article.**

[Begin typing in the editor, narrating each piece as you add it.]

Inside the body, add a br tag first to push things down from the very top of the page. Then open a center tag, add an img tag pointing to the ct-bugs.gif in the assets folder — give it its width and height of 161 by 27, and an alt of "Bugs Bunny." Close the center tag.

Now open the blockquote. Inside it, add the character photo — that is c-bugs.jpg from assets, 270 pixels wide by 206 pixels tall. Notice the align attribute is set to left. That tells the browser to float the image to the left side and let the text wrap around it on the right. The vspace and hspace attributes add some breathing room around the image so the text does not crowd it.

After the image, add a br tag, then the sub-heading "The Rabbit" in bold, followed by a p tag to end that line.

**Step 3 — Add the bio text.**

[Paste in the bio content. Highlight a few notable spots as you narrate.]

Now we paste in the article text. It is long, so go ahead and copy it from the lesson file. As you paste it in, notice a few things:

Where the movie title "Space Jam" appears, it is wrapped in b and then i — bold italic. Look for that pattern throughout.

Where the screenwriter names are joined by "and," the ampersand is written as an entity — ampersand, a-m-p, semicolon. That is how the original file handles it.

Each paragraph ends with a p tag rather than being fully wrapped. That is the nineties style and we are keeping it.

**Step 4 — Close the blockquote.**

[Continue in the editor after the last line of text.]

After the last line of the article, close the blockquote tag and add two br tags for spacing.

**Step 5 — Add the navigation footer.**

[Scroll to the bottom of the completed file and show the footer line.]

The footer is one long line inside a center tag. Open center, then open nobr — and here is the important part: everything inside nobr needs to be continuous, with no extra whitespace between elements. The left image, then the copyright font tag with the entity, then the right image, then close nobr.

Let me point out the align attribute on both images — it is set to "absmiddle." That vertically aligns the images to the middle of whatever text sits next to them, so the copyright notice lines up with the center of the buttons rather than hanging at the top or bottom.

Save the file and open it in your browser.

[Show the browser rendering of the completed page.]

You should see the title graphic at the top, the character photo floating left with the article text wrapping around it, bold sub-headings throughout, and the navigation footer at the bottom.

---

## Wrap-up

[Show the completed/bugs.html side by side with the student's version.]

Your page should match this. No color yet — black text on white — but the full structure is there.

In Module 3 we go back to the home page and apply the full Space Jam look: the black starfield, the logo, and the red text. That is where the visual identity of the site starts coming together.

See you there.
