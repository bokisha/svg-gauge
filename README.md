# SVG Gauge
Minmalistic, configurable, animated SVG gauge. Zero dependencies


### Usage

HTML
```html
<div id="cpuSpeed" class="gauge-container"></div>
```
CSS
```css
.gauge-container {
  width: 150px;
  height: 150px;
  display: block;
  padding: 10px;
}
.gauge-container > .gauge > .dial {
  stroke: #eee;
  stroke-width: 20;
  fill: rgba(0,0,0,0);
}
.gauge-container > .gauge > .value {
  stroke: rgb(47, 227, 255);
  stroke-width: 20;
  fill: rgba(0,0,0,0);
}
.gauge-container > .gauge > .value-text {
  fill: rgb(47, 227, 255);
  font-family: sans-serif;
  font-weight: bold;
  font-size: 10em;
}
```
Javascript
```js
// Require JS
var Gauge = require("svg-guage");

// Standalone
var Gauge = window.Gauge;

// Create a new Gauge
var cpuGauge = Gauge(document.getElementById("cpuSpeed"), {
    min: 0
    max: 100,
    value: 50,
});

// Set gauge value
cpuGauge.setValue(75);

// Set value and animate (value, animation duration in seconds)
cpuGauge.gauge1.setValueAnimated(90, 1);

```

#### Options

|      Name            |                  Description                       |
| -------------------- | ------------------------------------------------------------------------------------- |
| ```dialStartAngle``` | The angle in degrees to start the dial (```135```)       |
| ```dialEndAngle```   | The angle in degrees to end the dial. This MUST be less than dialStartAngle (```45```)  |
| ```radius```         | The radius of the gauge (```400```) |
| ```max```            | The maximum value for the gauge (```100```)  |
| ```showValue```      | Whether to show the value at the center of the gauge (```true```) |




#### [Live Demo](http://codepen.io/naikus/pen/BzkoLL)