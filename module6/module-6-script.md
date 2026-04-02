# Module 6 Script: Tables

---

## Intro

Welcome back. In Module 5 we got all eleven section buttons onto the home page. They were just lined up in a row. In this module we are going to use an HTML table to put them exactly where they belong — orbiting the Space Jam logo.

[Show the completed/index.html in a browser side by side with the original fullsite/index.html.]

These should look nearly identical. That layout — the logo in the center with the section buttons positioned around it at different corners and edges — is all done with a single table. Let's learn how.

---

## How Tables Work

[Open a simple example in the editor — or draw on screen if possible.]

An HTML table is built from three nested tags. The table tag is the outer container. Inside it, tr tags define rows. Inside each tr, td tags define individual cells. Every cell sits at the intersection of a row and a column. Columns are implied — the browser figures out how many columns there are by counting the td tags in each row.

Here is the simplest possible table: one row, two cells side by side.

[Show on screen: table tag, one tr, two td tags with simple content.]

That is the foundation. Everything else is just adding attributes to control size, spacing, and alignment.

---

## Table Attributes

[Open the completed/index.html in a text editor. Point to the opening table tag.]

Look at the table tag on the home page. It has width=500 and border=0.

Width sets how wide the table is. 500 pixels is enough to contain the logo and the surrounding buttons.

Border controls the visible grid lines around cells. Set it to zero. Layout tables — tables used for positioning rather than displaying data — should be invisible. Their purpose is to place things, not to draw boxes.

Cellpadding and cellspacing control spacing. Cellpadding is the space between a cell's content and its edges. Cellspacing is the gap between adjacent cells. Both are set to zero here so the button images sit exactly where we put them with no accidental gaps.

---

## Cell Attributes

[Scroll through the table in the completed file, pointing to individual td tags.]

The real work happens on the td tags. The align attribute sets horizontal alignment of the cell's content — left, center, or right. Valign sets vertical alignment within the cell — top, middle, or bottom. These two together let you position the image anywhere within its cell.

Width on a td sets how wide that column is. You will see some cells have an explicit width and others do not.

The two most powerful cell attributes are colspan and rowspan.

[Point to the td that contains the logo — it has colspan=3 and rowspan=2.]

Colspan makes a cell span across multiple columns. This logo cell spans three columns — it occupies the space of three normal cells side by side. Rowspan makes a cell span multiple rows — this cell also spans two rows, so the logo takes up a tall vertical area in the center of the table.

These two attributes together are what allow the logo to sit in the center while the buttons arrange themselves around it.

---

## Tables for Layout

[Step back and show the full table structure in the completed file.]

Let me orient you to the overall structure before we build it.

The table has five columns and four rows. The five columns have varying widths depending on what's in them.

Row one is a single spanning cell across all five columns — it is empty right now but in the full site it held a banner graphic.

Row two has four cells across: the Press Box button on the left spanning two columns, then Jam Central, Planet B-Ball, and Lunar Tunes across the right side.

Row three is where the logo enters. The Lineup button is in the leftmost column. Then the logo cell, spanning three columns wide and two rows tall, dominates the center and right. Jump Station sits in the far right column.

Row three and four share the logo span. In row four, Junior Jam is on the left. Then the Studio Store button, which spans two rows itself. Then the remaining columns run into row five.

Row five finishes with Souvenirs, Site Map, and Behind the Jam.

I know that sounds like a lot. Follow along in the completed file as we build it and it will make sense step by step.

---

## Exercise Walkthrough

Create a new index.html.

**Step 1 — Start from Module 5.**

[Open the Module 5 completed file for reference.]

Copy your Module 5 page as the starting point. It has the background, the logo, and the flat row of eleven buttons. We are going to remove that flat row and replace it with the table.

**Step 2 — Remove the flat button row.**

[Find and select the center block with all eleven images.]

Delete the center tag and all eleven bare img tags. The copyright footer stays. The logo at the top stays. We are replacing just that section.

**Step 3 — Add the table.**

[Type the table structure, narrating each row.]

In place of the deleted section, add a center tag and inside it open a table tag with width=500 and border=0.

Now add the rows. For each row I am going to describe what goes in it — follow along in the completed file if you need to see the exact attributes.

Row one: a single td with colspan=5, align=right, valign=top. It is empty. Close the tr.

Row two: first td has colspan=2, align=right, valign=middle — inside it, three br tags for spacing and then the Press Box image. Second td is center, middle — Jam Central image. Third td is center, valign=top — Planet B-Ball. Fourth td is center, valign=bottom — two br tags then Lunar Tunes. Close the tr.

Row three: first td is align=middle, valign=top — two br tags then The Lineup. Then comes the logo td — this is the big one. It has colspan=3 and rowspan=2, align=right, valign=middle. Put the logo image here. Last td in this row is align=right, valign=bottom — Jump Station. Close the tr.

Row four: first td, align=center, valign=bottom — Junior Jam. Then a td with rowspan=2, align=center, valign=top — two br tags then Studio Store. The rowspan here means this cell carries down through row five. Close the tr.

Row five: one empty td for the column. Then td align=center, valign=top — Souvenirs. Then td align=center, valign=bottom — four br tags for spacing then Site Map. Then td align=center, valign=middle — Behind the Jam. Close the tr.

Close the table tag and the center tag.

**Step 4 — Save and compare.**

[Show the browser result next to fullsite/index.html.]

Save and refresh. The buttons should be arranged around the logo. Compare it to the original in fullsite/index.html — the positioning should match.

---

## Wrap-up

[Show the side-by-side comparison.]

This is the result of a fairly complex table. Fourteen cells across five rows, with colspan and rowspan values threading the logo through the middle. It took the Space Jam designers the same level of effort in 1996 — this was the only tool they had for layout.

In Module 7 we move to a section hub page and learn about image maps. See you there.
