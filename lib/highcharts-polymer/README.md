[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://www.webcomponents.org/element/anthfran/highcharts-polymer)

# \<highcharts-chart\>

Display an Instagram image post in your Polymer website

## Demo

https://www.webcomponents.org/element/anthfran/highcharts-polymer/demo/demo/index.html

## Installation

`bower install --save anthfran/highcharts-polymer`

## Usage

### Include this custom element
`<link rel="import" href="../bower_components/highcharts-polymer/highcharts-chart.html">`

### Add to your app
<!--
```
<custom-element-demo>
  <template>
    <script src="../webcomponentsjs/webcomponents-lite.js"></script>
    <link rel="import" href="highcharts-chart.html">
    <next-code-block></next-code-block>  
    </template>
</custom-element-demo>
```
-->
```html
<highcharts-chart
  series='[{"name":"Installation","data":[43934,52503,57177,69658,97031,119931,137133,154175]},{"name":"Manufacturing","data":[24916,24064,29742,29851,32490,30282,38121,40434]},{"name":"Sales & Distribution","data":[11744,17722,16005,19771,20185,24377,32147,39387]},{"name":"Project Development","data":[null,null,7988,12169,15112,22452,34400,34227]},{"name":"Other","data":[12908,5948,8105,11248,8989,11816,18274,18111]}]'
  title='Solar Employment Growth by Sector, 2010-2016'
  subtitle='Source: thesolarfoundation.com'
  y-axis='Number of Employees'
  >
</highcharts-chart>
```
## History
Mar 14, 2018 - Initial release
