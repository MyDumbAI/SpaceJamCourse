# Module 7 Script: Image Maps

---

## Intro

Welcome back. Every section of the Space Jam site has a hub page — a landing page for that section with a large graphic and several links to sub-pages. The clever part is that instead of separate button images, these hubs use a single image with invisible clickable regions drawn on top of it.

[Show completed/jamcentral.html in a browser. Hover over different parts of the image to show the cursor changing.]

This is the Jam Central hub. It looks like a single image, and it is — one JPEG file. But there are four separate clickable zones mapped to different destinations: Production Notes, Photos, Filmmakers, and the Theatrical Trailer. That is an image map.

---

## What is an Image Map?

An image map lets you define multiple clickable regions within a single image, each linking to a different page. You draw invisible hotspot shapes over the image using pixel coordinates, and each shape becomes an independent link.

This technique was widely used in 1990s web design for navigation graphics — the designer could create one elaborate illustration and then the developer would map interactive zones onto it.

[Point to the Jam Central image. Hover to show all four clickable areas.]

You can see the four zones here. The cursor changes when you move over any of them. Under the hood, each zone has a set of coordinates describing its shape, and an href telling the browser where to go.

---

## The map and area Tags

[Open completed/jamcentral.html in a text editor. Point to the map tag and the area tags inside it.]

The image map is defined by a map tag. It has a name attribute — here it is just "map." Inside the map tag are area tags, one for each clickable region.

Each area tag has four attributes.

Shape describes the geometry of the hotspot. The most common is rect for rectangle. The others are circle and poly for polygon.

Coords gives the pixel coordinates that define the shape. For a rectangle, that is four numbers: the x position of the left edge, the y position of the top edge, the x of the right edge, and the y of the bottom edge. All measured in pixels from the top-left corner of the image.

Href is the destination — same as on a regular link tag.

Target works the same as on a link tag too. These all use target="_top" to break out of any frames.

---

## Connecting Image to Map

[Point to the img tag and its usemap attribute, then trace it to the map name.]

The img tag and the map tag are connected through the usemap attribute. On the img tag, usemap="#map" points to a map element named "map." The hash sign is required — it works like a page anchor.

The map tag itself can be placed anywhere in the document — the connection is made by name, not by position. The Space Jam site puts the map immediately after the img tag, which is the most readable convention.

---

## Finding Coordinates

One thing the lesson mentions that is worth emphasizing: the coordinates for each area have to be measured from the actual image.

[Open m-central.jpg in an image viewer or editor.]

When you look at this image, you can see labels printed on it: "production notes," "photos," "filmmakers," "trailer." Each label sits inside the region you want to make clickable. To find the correct coordinates, you open the image in any image editor, hover over the corners of each region, and read the pixel positions from the status bar. Most editors show x and y as you move the cursor.

[Show the image with an approximate overlay of where the rectangles are, if possible.]

For this image, the coordinates are already worked out in the lesson file. In the real world, finding these coordinates is a manual process of measuring in your image editor.

---

## Exercise Walkthrough

Let's build the Jam Central hub page. Create a new file called jamcentral.html.

**Step 1 — Page setup.**

[Create the file in the editor.]

Title it "Jam Central." Apply the Space Jam body attributes — black background, the bg_stars.gif tile, red text and links.

**Step 2 — The image and map.**

[Type the body content.]

Inside the body, add a br, then open a blockquote and a center tag. Add the m-central.jpg image tag: height 301, width 438, border=0, alt "navigation map", and usemap="#map".

Immediately after the img tag — still inside the center — add the map tag with name="map." Inside it, add four area tags. Each one uses shape="rect" and target="_top." The coordinates for each area are in the lesson file — copy them exactly.

[Point to the four area tags in the completed file as reference.]

Close the map, add a br, and close the center tag.

**Step 3 — Description text.**

After the center tag, still inside the blockquote, add the introductory paragraph. It is set in font size +2, so it is larger than body text — this is a feature introduction. The text starts with "You've made it: Jam Central Station..." Copy it from the lesson file.

Close the blockquote.

**Step 4 — Footer.**

Add a centered copyright footer in yellow — this section uses color #ffff00 for the copyright text instead of the usual white. That is a deliberate design choice in the original.

**Step 5 — Test.**

[Save and open in a browser. Hover over the image.]

Open the page. Move your cursor over the image. You should see it change to a pointer over the four labeled areas and stay as an arrow everywhere else. The hotspots are working.

If you click one of the areas, the browser will try to navigate to the linked page. Those pages do not exist yet — that is expected.

---

## Wrap-up

[Show the completed/jamcentral.html alongside the original fullsite/cmp/jamcentral/jamcentral.html in a browser.]

They should look identical. This hub page is used inside a frameset in Module 8 — it becomes the content that loads on the right side when the user arrives at Jam Central.

See you in Module 8 where we put this page inside a frame.
