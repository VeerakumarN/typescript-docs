---
layout: post
title: getting-started
description: getting started
platform: typescript
control: navigation drawer
documentation: ug
---

# Getting Started

This section helps you to understand the getting started of the Navigation Drawer control with the step-by-step instructions.

## Create a Navigation Drawer

The following steps guide you to add a Navigation Drawer control.

1)	Refer the common Typescript [Getting Started Documentation](https://help.syncfusion.com/js/typescript) to create an application and add necessary scripts and styles for rendering the Navigation Drawer control.

2)  Create an HTML page and add the scripts and css references in the order mentioned in the following code example.

{% highlight html %}

<!DOCTYPE html>
<html>
<head>
    <title>Typescript Application</title>
    <link href="http://cdn.syncfusion.com/**{{**site.releaseversion**}}**/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
    <script src="https://code.jquery.com/jquery-3.0.0.min.js"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jsrender.min.js" type="text/javascript"></script>
    <script src="http://cdn.syncfusion.com/**{{**site.releaseversion**}}**/js/web/ej.web.all.min.js" type="text/javascript"></script>
</head>
<body>
    <!--Add Navigation Drawer code here-->
</body>
</html>

{% endhighlight %}

3)	To display the navigation list item by using items property and also you can access the ListView control properties by enabling the enableListView property. Add the following code with in the <body> tag to render the Navigation Drawer with the list view items. 

    {% highlight html %}

        <div id="navpane">
          <ul>
             <li data-ej-text="Home"></li>
             <li data-ej-text="People"></li>
             <li data-ej-text="Profile"></li>
          </ul>
       </div>

    {% endhighlight %}

Create the target element as follows to display the list items by clicking target icon.

{% highlight html %}

    <div id="container">
        <div class="e-lv">
            <div class="e-header">
                <div id="butdrawer"
                     class="drawericon e-icon">
                </div>
            </div>
        </div> 
    </div>

{% endhighlight %}

Initialize the Navigation Drawer in ts file by using the ej.NavigationDrawer method.

{% highlight ts %}

    /// <reference path="../tsfiles/jquery.d.ts" />
 /// <reference path="../tsfiles/ej.web.all.d.ts" />\

module NavigationDrawerComponent {
    $(function () {
        var navigationdrawerInstance = new ej.NavigationDrawer($("#navpane"), {
            type: "overlay",
            direction: "left",
            enableListView: true,
            listViewSettings: {
                width: 300,
                selectedItemIndex: 0
            },
            position: "normal"
        });
    });
}

{% endhighlight %}

To set the target icon image and with the correct position as using the below mentioned styles .

{% highlight css %}

    <style>
    
      .drawericon {
        background-position: center center;
        background-repeat: no-repeat;
        height: 32px;
        width: 32px;
        background-size: 100% 100%;
        padding-right: 10px;
     }
     .drawericon:before {
        content: "\e76b";
        font-size: 28px;
        height: 26px;
     }

    </style>

{% endhighlight %}

![](Getting-Started_images/getting-started_img1.png)

To open the list items by clicking on target element using the targetId property.  

{% highlight ts %}

 /// <reference path="../tsfiles/jquery.d.ts" />
 /// <reference path="../tsfiles/ej.web.all.d.ts" />\

module NavigationDrawerComponent {
    $(function () {
        var navigationdrawerInstance = new ej.NavigationDrawer($("#navpane"), {
           targetId: "butdrawer",
            type: "overlay",
            direction: "left",
            enableListView: true,
            listViewSettings: {
                width: 300,
                selectedItemIndex: 0
            },
            position: "normal"
        });
    });
}
  
{% endhighlight %}

![](Getting-Started_images/getting-started_img2.png)

To set the images for list items of the Navigation Drawer by using the data-ej-imageclass property as follows.

{% highlight html %}

   <div id="navpane">
        <ul>
            <li data-ej-imageclass="icon-home" data-ej-text="Home"></li>
            <li data-ej-imageclass="icon-photos" data-ej-text="Photos"></li>
            <li data-ej-imageclass="icon-profile" data-ej-text="Profile"></li>
        </ul>
    </div>

{% endhighlight %}

You can set the images with the correct position by using the mentioned styles.

{% highlight css %}

    <style>
    
       #navpane [class*="icon-"] {
           width: 40px;
           height: 29px;
           background-image: url("http://js.syncfusion.com/ug/web/content/drawer/sprite.png");
       }

       .icon-home {
           background-position: 0 1px;
       }

       .icon-profile {
           background-position: 0px -532px;
       }

       .icon-photos {
           background-position: 0 -140px;
       }

    </style>

{% endhighlight %}

![](Getting-Started_images/getting-started_img3.png)


N> You can find the Navigation Drawer control properties from the [API reference](https://help.syncfusion.com/api/js/ejnavigationdrawer).