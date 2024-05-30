# martini-glass-simulation
Using vanilla JS



## notes
- calc max volume of cone w h=100
- calc vilume created by upside down cone, so max V - V of new height
- percentage = new volume / max volume
- apply percentage to second trisngle height

## notes 2
- f(h) to area
- f(h) to volume
- f(voulme) to h2
- f(h2) to area

todo: draw canvas

todo: draw two trianles

todo: draw vertical slide

todo: 
in vanilla javascript a 800x600 canvas

erneath the canvas draw a slider

as the slider moves fill the triable

when slider moves, fill trianlge to certain heights



## gemini prompts
In vanilla JavaScript, draw a 800x600 canvas
und

In vanilla JavaScript, write an html slider which determines how much a a white trianoe  is filled  with blue. For example, if the slider is up halfway then the triangle should be 50% filled (starting from the base). If the slider is only 25% up then the triangle should only 25% filled (starting from the base). 

## temp
You can achieve this using HTML, CSS, and JavaScript. Here's an example code snippet:

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Triangle Filling Slider</title>
<style>
  #triangle {
    width: 0;
    height: 0;
    border-left: 100px solid transparent;
    border-right: 100px solid transparent;
    border-bottom: 200px solid white; /* You can adjust the size of the triangle here */
    position: relative;
  }
  #fill {
    position: absolute;
    bottom: 0;
    left: 0;
    height: 0;
    width: 100%;
    background-color: blue;
  }
</style>
</head>
<body>
<input type="range" min="0" max="100" value="0" id="slider">
<div id="triangle">
  <div id="fill"></div>
</div>

<script>
  const slider = document.getElementById('slider');
  const fill = document.getElementById('fill');

  slider.addEventListener('input', () => {
    const fillPercentage = slider.value;
    fill.style.height = `${fillPercentage}%`;
  });
</script>
</body>
</html>
```

This code creates an HTML slider and a white triangle filled with blue. The JavaScript part updates the height of the blue fill div according to the slider value.



## inspiration from
https://youtu.be/Mkn3PzdaByY?si=TcBpY0Q-d1pu9k8u
