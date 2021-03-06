# ng-apexcharts

ng-apexcharts is an implementation of apexcharts for angular.
It comes with one simple component that enables you to use apexcharts
in an angular project.

## Installation

1. Install using npm:

````
npm install apexcharts ng-apexcharts --save
````

2. Open angular.json and under scripts add:

````
"scripts": [
  "node_modules/apexcharts/dist/apexcharts.min.js"
]
```` 

3. Add ng-apexcharts-module to imports

````
imports: [
  BrowserModule,
  FormsModule,
  ReactiveFormsModule,
  NgApexchartsModule,
  ...
]
````

## Usage

In any component you can use the chart using:

````
<apx-chart></apx-chart>
````

### Options

All options of the chart can inserted using the attributes.
This is a list of all available attributes:

````
@Input() chart: ApexChart;
@Input() annotations: ApexAnnotations;
@Input() colors: string[];
@Input() dataLabels: ApexDataLabels;
@Input() series: ApexAxisChartSeries | ApexNonAxisChartSeries;
@Input() stroke: ApexStroke;
@Input() labels: string[];
@Input() legend: ApexLegend;
@Input() fill: ApexFill;
@Input() tooltip: ApexTooltip;
@Input() plotOptions: ApexPlotOptions;
@Input() responsive: ApexResponsive[];
@Input() xaxis: ApexXAxis;
@Input() yaxis: ApexYAxis | ApexYAxis[];
@Input() grid: ApexGrid;
@Input() states: ApexStates;
@Input() title: ApexTitleSubtitle;
@Input() subtitle: ApexTitleSubtitle;
@Input() theme: ApexTheme;
````


### Use methods

If you want to access the methods of the components use this in your component:
````
@ViewChild('chartObj') chart: ChartComponent;
````

and change the template to this:
````
<apx-chart #chartObj></apx-chart>
````

## Author

[Morris Janatzek](http://morrisj.net) ([morrisjdev](https://github.com/morrisjdev))
