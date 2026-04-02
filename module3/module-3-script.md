# Module 3 Script: Colors & Backgrounds

---

## Intro

Welcome back. We have a skeleton and we have a content page. Now we are going to make something that actually looks like the Space Jam site.

[Show the completed/index.html file rendered in a browser.]

This is what we are building in this module. Black background, star field, the Space Jam logo centered on the page. By the end of this, if you put your version next to the original, they are going to look nearly identical in terms of visual atmosphere.

We are covering three things: how 1996 HTML handles color, how hex color codes work, and how background images tile across a page. Let's go.

---

## Color on the body Tag

[Open the completed/index.html file in a text editor. Point to the body tag at the top of the file.]

In modern web development, color and styling are handled by CSS — a separate language that lives in its own file or its own section of the page. But in 1996, none of that existed the way it does today. Color was applied directly to HTML tags as attributes.

The most important place to set color is the body tag. Look at this body tag — it has a lot going on. Let's go through each attribute one at a time.

The first one is bgcolor. That sets the background color of the entire page. You can see it is set to six zeros with a hash in front — we will talk about what that means in a moment, but that is black.

The next one is background. This one points to an image file. The browser loads that image and tiles it — repeats it over and over — to cover the entire background of the page. You can see it is pointing to the bg_stars.gif file in the assets folder.

Then there is text. That sets the color of all regular body text on the page. Everything the user reads inherits this color by default.

After that are three link attributes: link, vlink, and alink. Link is the color of links the user has not clicked yet. By default browsers show those as blue. Vlink — visited link — is what color a link turns after the user has been there. And alink — active link — is the color it flashes for the instant the user is clicking it. In the Space Jam site all three are set to the same reddish color, so links look consistent regardless of state.

One body tag. Six attributes. The entire color scheme of the page set in one line.

---

## Hex Color Codes

[Keep the body tag visible in the editor. Point to the color values as you describe them.]

Let's talk about those color values. They all start with a hash sign followed by six characters. These are hexadecimal color codes, and they are the standard way to write colors in HTML.

Hexadecimal is a base-16 number system. Instead of zero through nine, it goes zero through nine and then A through F, giving you sixteen possible values per digit. The six characters in a color code are split into three pairs — the first pair represents red, the second green, the third blue. Each pair can go from zero-zero, which is none of that color, to F-F, which is the maximum.

[Point to the bgcolor value of #000000.]

So this one — zero-zero, zero-zero, zero-zero — is zero red, zero green, zero blue. That is black.

[Point to the text color value of #ff0000.]

This one — F-F, zero-zero, zero-zero — is maximum red, no green, no blue. Pure red. That is the body text color.

[Point to the link color value of #ff4c4c.]

And this one — F-F, four-C, four-C — is still mostly red, but with a small amount of green and blue added in. That makes it a slightly softer, less saturated red. Used for the links so they are still in the red family but visually distinct from the body text.

You do not need to calculate these values by hand. Any color picker — including ones built into browsers — will give you the hex code for any color you choose. What matters is that you understand the format: hash, then six hex digits, two each for red, green, and blue.

---

## Background Images

[Show the bg_stars.gif file on its own, then show the completed page in the browser.]

The background attribute on the body tag takes a path to an image file, and the browser tiles it to fill the entire page. It repeats the image horizontally until it fills the window width, then repeats that row of tiles vertically until the page is covered — top to bottom, edge to edge, no matter how big the window is or how long the page gets.

[Point to the small size of bg_stars.gif if you can show it at its actual dimensions.]

The star field image is quite small. You can see it is a dark tile with just a few white dots. But because it tiles seamlessly, the result is a continuous star field across the whole page. The original designers made the tile small to keep the file size down — this site was designed for dial-up connections.

[Return to the body tag in the editor.]

Notice that both bgcolor and background are set. That is intentional. The background color appears immediately when the page loads, before the browser has downloaded the image. If you only set the image, there is a flash of white while it loads. Setting bgcolor to black means the page background is already black from the very first millisecond, and the stars just appear on top of it. No flash.

---

## Images

[Scroll to the img tag for the logo in the completed file.]

You have seen the img tag used as a placeholder in earlier modules. Here we are actually placing the Space Jam logo, so let's walk through the attributes properly.

The src attribute is the path to the image file. It is relative to the HTML file — so this path, assets slash p-jamlogo.gif, means "look for a folder called assets next to this HTML file, and inside it find p-jamlogo.gif."

The width and height attributes set the dimensions in pixels. You should always include these. When the browser knows how big an image will be before it downloads, it reserves that space in the layout immediately. Without them, the page layout can jump around as images load in, which looks broken and unprofessional.

The alt attribute is the alternative text. It is a plain-English description of what the image shows. This is what appears if the image fails to load, and it is what screen readers use to describe the image to users who cannot see it.

And border equals zero removes a border that browsers automatically draw around images when they are inside a link. Without it you would see a colored rectangle around the logo. You will see border equals zero on almost every image in the Space Jam site.

---

## Assets

[Open the assets/ folder for this module.]

The assets folder for this module has two files.

The bg_stars.gif is the small tileable star field image. The p-jamlogo.gif is the Space Jam logo that will be centered on the page.

---

## Exercise Walkthrough

Let's build it. Create a new file and save it as index.html.

**Step 1 — Start from the skeleton.**

[Show the Module 1 completed/index.html for reference.]

Paste in the Module 1 skeleton — the comment, html, head, title, body, and the h1 heading. We are starting from where we left off in Module 1.

**Step 2 — Add the color scheme.**

[Focus on the body tag in the editor.]

Find the plain body tag and replace it with the full version. Add bgcolor and set it to six zeros with a hash — that is black. Add background and point it to assets/bg_stars.gif. Add text and set it to the red hex code — hash, F-F, zero-zero, zero-zero. Then add link, vlink, and alink and set all three to hash, F-F, four-C, four-C — the slightly softer red for links.

Save the file and open it in your browser.

[Show the browser result.]

The page is black with stars tiling the background. The heading "Space Jam" is showing in red. All six of those body attributes are working at once.

**Step 3 — Replace the heading with the logo.**

[Return to the editor and find the h1 tag.]

The h1 was a placeholder. Delete it. In its place, add a center tag and inside it put the img tag for the logo. The src points to assets/p-jamlogo.gif. Give it a width of 272, a height of 165, an alt of "Space Jam," and border equals zero. Close the center tag.

Save and refresh.

[Show the browser.]

The text heading is gone and the logo appears centered on the star field. This is starting to look like the actual site.

**Step 4 — Add the copyright footer.**

[Return to the editor, below the center tag for the logo.]

Add two br tags for spacing, then open another center tag. Inside it, put a font tag with size set to negative one. Inside the font tag, write the trademark notice on two lines — use a br tag to break between "SPACE JAM, characters, names, and all related" and "indicia are trademarks of Warner Bros." After "Warner Bros." add the copyright entity — that is ampersand, c-o-p-y, semicolon — then the year 1996. Close the font tag, add one more br, and close center.

Save and refresh.

[Show the completed browser view.]

The logo is centered on the star field. Below it, in small red text, is the trademark notice on two lines. That is the full Space Jam visual identity.

---

## Wrap-up

[Show the completed/index.html in the browser alongside the student's version.]

Your result should match this. Now open the fullsite/index.html — the actual archived page — and compare.

[Show both side by side if possible.]

The real home page has navigation buttons arranged around the logo and a couple of ad slots. Those pieces require tables, which we cover in Module 6, and links from Module 4. But the atmosphere of the page — the color, the background, the logo, the feel — that is exactly what you have built here.

In Module 4 we add links and things start connecting into a real navigable site.

See you there.
