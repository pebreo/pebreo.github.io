
## prompt
in vanilla javascript, write a 640x480 black canvas in the center of an html page. also draw a white outline circle (5 pixel thick outline)

Here's the HTML code for the webpage:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Canvas Example</title>
</head>
<body>
    <canvas id="myCanvas"></canvas>
    <script src="script.js"></script>
</body>
</html>
```

This code creates a basic HTML structure with a canvas element with the ID "myCanvas". 

Here's the JavaScript code for the script.js file:

```javascript
const canvas = document.getElementById('myCanvas');
const ctx = canvas.getContext('2d');

// Set the canvas dimensions to 640x480
canvas.width = 640;
canvas.height = 480;

// Get the center coordinates of the canvas
const centerX = canvas.width / 2;
const centerY = canvas.height / 2;

// Set fill style for background to black
ctx.fillStyle = 'black';

// Fill the rectangle to cover the entire canvas
ctx.fillRect(0, 0, canvas.width, canvas.height);

// Set stroke style for the circle outline to white
ctx.strokeStyle = 'white';

// Set line width for the outline to be 5 pixels thick
ctx.lineWidth = 5;

// Calculate the radius for the circle (considering half the line width for the outline)
const radius = Math.min(centerX - ctx.lineWidth / 2, centerY - ctx.lineWidth / 2);

// Draw the circle outline
ctx.beginPath();
ctx.arc(centerX, centerY, radius, 0, 2 * Math.PI);
ctx.stroke();
```

This JavaScript code:

1. Gets a reference to the canvas element using its ID.
2. Gets the 2D context of the canvas for drawing.
3. Sets the width and height of the canvas to 640 and 480 respectively.
4. Calculates the center coordinates of the canvas.
5. Sets the fill style for the background to black.
6. Fills a rectangle with the black color to cover the entire canvas area.
7. Sets the stroke style for the circle outline to white.
8. Sets the line width for the outline to be 5 pixels.
9. Calculates the radius of the circle considering half the line width for the outline to stay within the canvas boundary.
10. Starts a new path for drawing the circle.
11. Uses the `arc` method to draw an arc representing the circle outline. The arguments are center coordinates, radius, starting angle (0), ending angle (2π for full circle), and direction (counter-clockwise).
12. Strokes the path to draw the white outline circle.

## video
https://www.youtube.com/watch?v=uXSPWOjav-w
