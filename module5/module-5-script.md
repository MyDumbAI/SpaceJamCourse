# Module 5 Script: Images

---

## Intro

Welcome back. In Module 3 we put the Space Jam logo on the home page. In this module we are adding the rest of the images — all eleven section buttons that orbit the logo. By the end you will have every image asset on the home page loading correctly.

[Show the completed/index.html in a browser — all buttons present but in a flat row, not the orbital layout.]

This is where we land today. All the images are here, all loading, but they are just lined up in a row. They are not in the right positions yet — that is what Module 6 and its tables are for. Today is about getting comfortable with the img tag in full.

---

## img Attributes in Full

[Open the completed/index.html in a text editor. Point to one of the img tags.]

You have seen the img tag in every module so far, but we have been using it without explaining everything it can do. Let's go through all the attributes now.

src is the path to the image file. You already know this one.

alt is the alternative text. It is a plain-English description of the image. It shows when the image fails to load and it is what screen readers use to describe the image to people who cannot see it. Always include it.

width and height set the dimensions in pixels. Here is why these matter: when the browser starts loading a page, it lays out the content before all the images have downloaded. If it does not know how big an image will be, it leaves zero space for it and then jumps the layout around when the image finally arrives. If you specify the dimensions up front, the browser reserves exactly that space immediately. The page loads smoothly instead of jumping.

border controls the border drawn around the image. Set it to zero. On a bare image it does nothing visible, but it prevents the colored link-border from appearing if you later wrap the image in a link.

align — and this one has several values worth knowing. On the Bugs bio page in Module 2, we used align equals left on the character photo. That floated the image to the left margin and let the article text wrap around it on the right side. You can also use align equals right to float the other direction.

[Point to align=absmiddle usage in the footer of the bio page if visible.]

There is also align equals absmiddle, which you saw in the footer of the bio pages. This vertically aligns the image to the middle of the text sitting next to it. Without it, images in a line of text sit at the baseline — the bottom of the text — which looks awkward. Absmiddle keeps everything visually centered on the same horizontal line.

hspace adds horizontal space on both sides of the image. vspace adds vertical space above and below. Both values are in pixels. They give images breathing room so content does not crowd right up against them.

---

## GIF vs. JPG

[Show the assets folder. Point to some GIF files and some JPG files.]

The assets folder has both .gif and .jpg files. Let's talk about when each is used.

GIF is best for images with flat areas of solid color — logos, icons, buttons, illustrations, anything with sharp edges and a limited color palette. GIF also supports transparency, so you can have images with irregular shapes that show the background through them. And GIF supports simple animation. Almost all the navigation buttons and title graphics in the Space Jam site are GIFs.

JPG is best for photographs and images with gradients and continuous color — things with a lot of tonal variation. JPG compresses photographic content efficiently in a way that GIF cannot. The character photos, the background starfield JPEG, and photographic elements are all JPGs.

As a rule of thumb: if it is a drawing, a logo, or a button, use GIF. If it is a photograph, use JPG.

---

## Organizing Assets in Folders

[Show the fullsite/img/ folder structure.]

In the real Space Jam site, every root-level image — the navigation buttons, the logo, the background tile — lives in a folder called img next to the home page. Section-specific images are in an img folder inside each section's own folder.

[Show the module5/assets/ folder.]

In our modules, we are using an assets folder at the module level. The principle is the same — you keep images in a dedicated folder rather than dumping them alongside your HTML files. When you write the src path, it just needs to accurately describe where the file is relative to the HTML file that references it.

---

## Exercise Walkthrough

Let's build the page. Create a new index.html.

**Step 1 — Start from Module 3.**

[Open the Module 3 completed/index.html for reference.]

Copy your Module 3 home page as the starting point. It has the black starfield body, the centered logo, and the copyright footer. We are adding the section buttons between the logo and the footer.

**Step 2 — Add the section buttons.**

[Begin typing in the editor, between the logo center block and the copyright footer.]

After the logo's closing center tag and a couple of br tags, open a new center tag. Now add each section button image one after another. For each one: img tag, src pointing to the correct file in assets, height and width as specified in the lesson, alt text describing the section, and border equals zero.

[Add a few, narrating each.]

Press Box: 131 wide by 56 tall, alt "Press Box."

Jam Central: 55 wide by 67 tall, alt "Jam Central."

Planet B-Ball: 62 by 62, alt "Planet B-Ball."

Continue through all eleven. The names are listed in the lesson file.

Close the center tag after the last image.

Save and open in the browser.

[Show the browser with all images loaded.]

All eleven buttons are visible. They are sitting in a horizontal flow — the browser is placing them next to each other until it runs out of room and wraps to a new line. They are not in the orbital arrangement yet, and that is fine. Every image is loading, every alt text is set, and every dimension is correct.

---

## Wrap-up

[Show the completed/index.html side by side with the student's result.]

Your page should match this. All eleven buttons present and accounted for.

In Module 6 we use an HTML table to position these images precisely — the Press Box off to the side, the logo in the center, the other buttons arranged around it. The finished result will match the original Space Jam home page layout.

See you there.
