## Charts

- Displaying data visually than tables and have the added benefit.

- To git started with chart first you need to download the Chart.js, and then create html page and import the script.

- To draw a line chart, drawing a pie chart,a bar chart we need to create canvas element in html and then the script then create the data inside the script too.

- To get started with chart the required is the script included and the <canvas> in the page. 


## Basic usage of canvas

- `<canvas>` `</canvas>` is HTML element that is look like to `<img>` but doesn't have `src` and `alt`, it has two attributes width and height.

- `<canvas>` can be styled just like the image but it differs from `<img>` it's more like `<video>`,`<audio>` or `<picture>` elements.

- `<canvas>` element create a fix-sized drawing surface expose rendering text.


### Drawing shapes using canvas

- `<canvas>` used to draw shapes like rectangles, triangles, lines and curves.

- We need to specify the gird dimensions (width and height).

- Drawing a rectangles:
    - fillRect(x, y, width, height): filled rectangle.
    - strokeRect(x, y, width, height): rectangular outline.
    ` clearRect(x, y, width, height) Clears the specified rectangular area, making it fully transparent.

- Drawing paths:
    - beginPath(): Creates a new path. 
    - Path methods: Methods to set different paths for objects.
    - closePath(): Adds a straight line to the path, going to the start of the current sub-path.
    - stroke(): Draws the shape by stroking its outline.
    - fill(): Draws a solid shape by filling the path's content area.

- Drawing circles and arcs:
    - arc(x, y, radius, startAngle, endAngle, counterclockwise): Draws an arc which is centered at (x, y) position with radius r starting at startAngle and ending at endAngle going in the given direction indicated by counterclockwise (defaulting to clockwise).
    - arcTo(x1, y1, x2, y2, radius) Draws an arc with the given control points and radius, connected to the previous point by a straight line.

- Moving pen function: it doesn't draw anything but it's part from the path. `moveTo(x, y)`

- Lines: drawing line by specify the current position x,y arguments.

- `<canvas>` using to draw many types of curves too like bezier, quadratic and cubic curves:
    - quadraticCurveTo(cp1x, cp1y, x, y)
    - bezierCurveTo(cp1x, cp1y, cp2x, cp2y, x, y)

- We can make a combination to draw many shapes by different paths and curves.


### Applying styles

- To apply colors to a shape there are two important properties we can use: fillStyle and strokeStyle.

- fillStyle = color: Sets the style used when filling shapes.
- strokeStyle = color: Sets the style for shapes' outlines.
- globalAlpha = transparencyValue values between 0-1.
- Applying lineWidth ,lineCap, lineJoin, miterLimit, lineDashOffset values to style lines.
- Gradients : createLinearGradient(x1, y1, x2, y2), createRadialGradient(x1, y1, r1, x2, y2, r2), createConicGradient angle, x, y)
- Creat patterns createPattern(image, type) and specify the repetition.


### Drawing and Styling texts
- fillText(text, x, y [, maxWidth])
- strokeText(text, x, y [, maxWidth])
- To edit font size, text-align, textBaseline and text's direction.


References:

#### References :
[Chart.js API](https://www.webdesignerdepot.com/2013/11/easily-create-stunning-animated-charts-with-chart-js/)
[Chart.js docs](https://www.chartjs.org/docs/latest/)
[Basic usage of canvas](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Basic_usage)
[Drawing shapes with canvas](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Drawing_shapes)
[Applying styles and colors](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Applying_styles_and_colors)
[Drawing text](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Drawing_text)