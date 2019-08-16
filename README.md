# SVG-GeoJSON-Plotter
This two files converts a table of rectangular coordinates and IDs and plot them on an SVG/GeoJSON files respectively. This save quite a lot of time in generating rectangular layouts

## Instructions
On the two Excel files, there is respectively a sheet named "list" with preset IDs and coordinates (only serve as placeholders). Paste or type your coordinates directly over
the old placeholder table. Make sure the whole set is being replaced.

On the sheet "svg_output"/"json_output" (depending on the format you choose), you can copy column A and paste it into your preferred text editor/IDE.
The GeoJSON/SVG file will be ready.

## Setting the Coordinates
For **SVG** version, the coordinates refer to the pixel with (0,0) at the top-left corner. So, to prevent complications it would be better to make the coordinates integral. It is a best preactice to maintain a margin so that the rectangles
does not sticks to the sides of the display.

For **GeoJSON** version, the coordinates are based on the World Map Earth system so you will need to be familar with longtitutes and latitutes of the Earth. If you are to work on geospatial data formats most likely you
 know how to handle those coordinates. As for non-experts, you may need to be aware that the range is bounded in [0,180] for both x and y coordinates. 
