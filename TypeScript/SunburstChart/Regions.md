---
layout: post
title: Sunburst elements 
description: Learn how to customize the sunburst segments 
platform: ts
control: SunburstChart
documentation: ug

---
 
# Sunburst Elements

The Sunburst region represents the entire chart and all its elements. It includes all the chart elements like Legend, DataLabel, Levels etc. The major properties of the Sunburst Chart are as follows

* `datasource`– Provides the data that are used to generate the chart.
* `valueMemberPath`- Property based on the which the data segments are rendered in the  Sunburst chart 
* `legend` – displays the legend of the Sunburst Chart
* `levels`- displays the hierarchical levels for the chart 
* `dataLabel` – displays the data label for the Sunburst Chart

## Start and End Angle
Start and End Angle

You can change the start and end angle of Sunburst chart using **startAngle** and **endAngle** property as shown in below code

{% highlight ts %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module  sunburstComponent {

$(function () {

var sample = new ej.datavisualization.SunburstChart($("#Sunburst"),{
          
          //Set startAngle and endAngle to draw the sunburst chart
         startAngle: -90, endAngle: 90          
         //..

        });
    });
}


{% endhighlight %}

## Sunburst Radius

 The Radius of the Sunburst chart can be customized by using the **radius** property. The default value of radius is 1 and its value ranges between 0 and 1 

{% highlight ts %}

$(function () {

var sample = new ej.datavisualization.SunburstChart($("#Sunburst"),{
          
           //Set radius to the sunburst chart
         radius: 0.8,        
         //..

        });
    });

{% endhighlight %}

![](Regions_images/Regions_img1.png);

 ## Sunburst Inner Radius
 
 The Inner Radius of the Sunburst chart can be customized by using the 
 **innerRadius** property. The default value of innerRadius is 0.4 and its value ranges between 0 and 1 

{% highlight ts %}

$(function () {

var sample = new ej.datavisualization.SunburstChart($("#Sunburst"),{
          
            //Set  inner radius to the sunburst chart
         innerRadius: 0.5,        
         //..

        });
    });

{% endhighlight %}

![](Regions_images/Regions_img2.png);




