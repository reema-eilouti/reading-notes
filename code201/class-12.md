# Class 12 Reading Notes

## Chart.js and Canvas

### HTML Canvas Graphics  
  
- The HTML `<canvas>` element is used to draw graphics on a web page, on the fly, via **JavaScript**.  

- The `<canvas>` element is only a *container* for graphics. You must use **JavaScript** to actually draw the graphics.  

  
#### Canvas Examples  

- A canvas is a rectangular area on an HTML page. By default, a canvas has no border and no content.  

- The markup looks like this: `<canvas id="myCanvas" width="200" height="100" style="border:1px solid #000000;"></canvas>`  

- Always specify an **id** attribute *(to be referred to in a script)*, and a **width** and **height** attribute to define the size of the canvas. To add a **border**, use the `style` attribute.  

#### Adding JavaScript  

- After creating the rectangular canvas area, you must add a JavaScript to do the drawing.

- Example *(to draw a line)*: 
```
<script>
var c = document.getElementById("myCanvas");
var ctx = c.getContext("2d");
ctx.moveTo(0, 0);
ctx.lineTo(200, 100);
ctx.stroke();
</script> 
```
  

### Chart.js  

- Simple yet flexible JavaScript charting for designers & developers.  

- It's easy to get started with **Chart.js**. All that's required is the **script** included in your page along with a single `<canvas>` node to render the chart.  

#### Example  

```
<canvas id="myChart" width="400" height="400"></canvas>
<script>
var ctx = document.getElementById('myChart').getContext('2d');
var myChart = new Chart(ctx, {
    type: 'bar',
    data: {
        labels: ['Red', 'Blue', 'Yellow', 'Green', 'Purple', 'Orange'],
        datasets: [{
            label: '# of Votes',
            data: [12, 19, 3, 5, 2, 3],
            backgroundColor: [
                'rgba(255, 99, 132, 0.2)',
                'rgba(54, 162, 235, 0.2)',
                'rgba(255, 206, 86, 0.2)',
                'rgba(75, 192, 192, 0.2)',
                'rgba(153, 102, 255, 0.2)',
                'rgba(255, 159, 64, 0.2)'
            ],
            borderColor: [
                'rgba(255, 99, 132, 1)',
                'rgba(54, 162, 235, 1)',
                'rgba(255, 206, 86, 1)',
                'rgba(75, 192, 192, 1)',
                'rgba(153, 102, 255, 1)',
                'rgba(255, 159, 64, 1)'
            ],
            borderWidth: 1
        }]
    },
    options: {
        scales: {
            yAxes: [{
                ticks: {
                    beginAtZero: true
                }
            }]
        }
    }
});
</script>
```

##### [Go Back](code_201_reading_notes.md)