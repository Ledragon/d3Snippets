#D3.js snippets
##Description
A set of snippets helping performing some common operations with [D3.js](d3js.org). These snippets works both with [TypeScript](typescriptlang.org) and Javacript (ES6 /ES2015 or above).

##Available Commands
`All commands start with the d3 prefix`

###d3LinearScale

Creates a linear scale.

Output:
```javascript
var scale = d3.scale.linear()
  .domain([0, 1])
  .range([0,width])
```

###d3LinearAxis

Creates a linear axis in a selection.

Output:
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
###d3Transform

Appends the `transform` attribute *in situ*.

Output:
```javascript
.attr('transform', `translate(${},${})`)
```
###d3Rect

Appends a rectangle to a selection.

Output:
```javascript
var rect = container.append('rect')
              .attr({
                'x': ,
                'y': ,
                'width': ,
                'height': ,
              });
              .style('fill', 'lightblue');
```
###d3Circle

Appends a circle to a selection.

Output:
```javascript
var circle = container.append('circle')
              .attr({
                'cx': ,
                'cy': ,
                'r': ,
              });
              .style('fill','lightblue');
```
