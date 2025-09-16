# Weather Report

```js
// creates a variable called forecast that stores the 
const forecast = FileAttachment("./data/forecast.json").json();
```

```js
display(
  Plot.plot({
    title: "Hourly temperature forecast",
    x: {type: "utc", ticks: "day", label: null},
    y: {grid: true, inset: 10, label: "Degrees (F)"},
    marks: [
      Plot.lineY(forecast.properties.periods, {
        x: "startTime",
        y: "temperature",
        z: null, // varying color, not series
        stroke: "temperature", // enable color encoding
        curve: "step-after"
  })
]
})

);
```