# D3.js snippets
## Description
A set of snippets for [Visual Studio Code](https://code.visualstudio.com) helping performing some common operations with [D3.js](https://d3js.org/). These snippets work both with [TypeScript](http://www.typescriptlang.org/) and Javacript (ES6 /ES2015 or above).

## Available Commands
`All commands start with the d3 prefix`

### d3LinScale (*v4 specific*)

Creates a linear scale.

**Output:**
```javascript
let scale = d3.scaleLinear()
    .domain([0, 1])
    .range([0,width]);
```
### d3LinAxis (*v4 specific*)

Creates a linear axis in a selection.

**Output:**
```javascript
let scale = d3.scaleLinear()
    .domain([0, 1])
    .range([0,width]);
let axis = d3.axisBottom(scale);
let axisGroup = container.append('g')
    .classed('axis', true)
    .call(axis);
```

### d3v3LinearScale (*v3 specific*)

Creates a linear scale.

**Output:**
```javascript
var scale = d3.scale.linear()
  .domain([0, 1])
  .range([0,width])
```

### d3v3LinearAxis (*v3 specific*)

Creates a linear axis in a selection.

**Output:**
```javascript
var scale = d3.scale.linear()
  .domain([0, 1])
  .range([0,width])
var axis = d3.svg.axis()
  .orient('bottom')
  .scale(scale);
var axisGroup = container.append('g')
  .classed('axis', true)
  .call(axis);
```

### d3Transform

Appends the `transform` attribute *in situ*.

**Output:**
```javascript
.attr('transform', (d, i) => `translate(${},${})`)
```

### d3Rect

Appends a rectangle to a selection.

**Output:**
```javascript
var rect = container.append('rect')
  .attr('x', )
  .attr('y', )
  .attr('width', )
  .attr('height', )
  .style('stroke','none')
  .style('fill','lightblue');
```
### d3Circle

Appends a circle to a selection.

**Output:**
```javascript
var circle = container.append('circle')
  .attr('cx', )
  .attr('cy', )
  .attr('r', )
  .style('stroke','none')
  .style('fill','lightblue');
```
### d3Bind

Creates an exit-enter stub.

**Output:**
```javascript
var dataBound = container.selectAll('.classed')
    .data(data);
dataBound
    .exit()
    .remove();
var enterSelection = dataBound
    .enter()
    .append('g')
    .classed('classed', true);
```
### d3Csv

Creates a stub to read a csv file.

**Output:**
```javascript
d3.csv('filename.csv',
(error, data) => {
   if (error) {
       console.error(error);
   } else {
       console.log(data);
   }
});
```

### d3Plot

Creates an svg,and a group with margins as a container for plotting purpose.

**Output:**
```javascript
let svg = d3.select('#chart')
    .append('svg')
    .attr('width', width)
    .attr('height', height);

let plotMargins = {
    top: 30,
    bottom: 30,
    left: 150,
    right: 30
};
let plotGroup = svg.append('g')
    .classed('plot', true)
    .attr('transform', `translate(${plotMargins.left},${plotMargins.top})`);

let plotWidth = width - plotMargins.left - plotMargins.right;
let plotHeight = height - plotMargins.top - plotMargins.bottom;
```