# SVG-GeoJSON-Plotter
This two xlsx files converts a table of rectangular coordinates and IDs and plot them on an SVG/GeoJSON files respectively. This save quite a lot of time in generating highly regular rectangular layouts. Some examples of use includes floorplan for carparks and warehouses.

## Instructions
In the two Excel files, there is respectively a sheet named "list" with preset IDs and coordinates (only serve as placeholders). Paste or type your coordinates directly over
the old placeholder table. Make sure the whole set is being replaced.

![Instruction1](/docs/instruction1.png)

On the sheet "svg_output"/"json_output" (depending on the format you choose), you can copy column A and paste it into your preferred text editor/IDE.
![Instruction2](/docs/instruction2.png)

The GeoJSON/SVG file will be ready. For effecient calcuation, only the first ~100,000 of lines on the "svg_output"/"json_output" sheet contain formula. If your list of IDs and coordinates is too long (>5,000 rows), and you find the output truncated, copy the formula and extend it to the bottom.

## Setting the Coordinates
For **SVG** version, the coordinates refer to the pixels on the screen with the origin (0,0) at the top-left corner. So, to prevent complications it would be better to make the coordinates integral. It is a best preactice to maintain a margin so that the rectangles
does not sticks to the sides of the display.

For **GeoJSON** version, the coordinates are based on the World Map Earth system so you will need to be familar with longtitutes and latitutes of the Earth. If you are to work on geospatial data formats most likely you
 know how to handle those coordinates. As for non-experts who are plotting without the geospatial context (just plotting some shapes around, not specifically on any part on the Earth), it is recommended to plot within the first quadrant (i.e. the red area below). Also, make sure the coordinates are close to zero to minimise the distortion of Mercator projection near 90° angle.
 
 ![Recommeded](/docs/recommendations.PNG)

## An Example
For better understanding of the instructions, here is an example of generating a SVG plot.

Suppose we need to make a sitting plan as follow.
![Layout](/docs/layout.PNG)

We will have to input the coordinates on the sheet 'list'.
![Step1](/docs/step1.PNG)

The sheet 'svg_output' will calculate and give the source code for SVG. Copy column A, make sure all the cells with content on column A are being copied. It is OK to copy excess empty cells.
![Step2](/docs/step2.PNG)

Paste the content on a text editor. Save it as an SVG file.
![Step3](/docs/step3.PNG)

The SVG generation is now complete!
![Example](/docs/example.PNG)
