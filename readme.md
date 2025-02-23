[![](https://raw.githubusercontent.com/timqian/images/master/20190819131226.gif)](https://timqian.com/chart.xkcd/)

## About

Chart.xkcd is a chart library plots “sketchy”, “cartoony” or “hand-drawn” styled charts.

Check out the [documentation](https://timqian.com/chart.xkcd/) for more instructions and links, or try out the [examples](./examples), or chat with us in [Slack](https://join.slack.com/t/t9tio/shared_invite/enQtNjgzMzkwMDM0NTE3LTE5ZTUzYjU4Y2I0YzRiZjNkYTkzMzE1ZmM0NDdmYzRlZmMxNGY1MzZlN2EwYjYyNWVlMWY0Nzk2MDBhNWZlY2I)

## Quick start

It’s easy to get started with chart.xkcd. All that’s required is the script included in your page along with a single `<svg>` node to render the chart.

In the following example we create a line chart.

> **[Preview and edit on codepen](https://codepen.io/timqian/pen/GRKqLaL)**

```html
<svg class="line-chart"></svg>
<script src="https://github.com/timqian/chart.xkcd/releases/download/1.0.1/chart.xkcd.js"></script>
<script>
  const svg = document.querySelector('.line-chart')

  new chartXkcd.Line(svg, {
    title: 'Monthly income of an indie developer',
    xLabel: 'Month',
    yLabel: '$ Dollors',
    data: {
      labels:['1', '2', '3', '4', '5', '6','7', '8', '9', '10'],
      datasets: [{
        label: 'Plan',
        data: [30, 70, 200, 300, 500 ,800, 1500, 2900, 5000, 8000],
      }, {
        label: 'Reality',
        data: [0, 1, 30, 70, 80, 100, 50, 80, 40, 150],
      }]
    },
  });
</script>
```
