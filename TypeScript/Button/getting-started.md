---
layout: post
title: Getting started with Typescript Button Control | Syncfusion
description: Learn here about getting started with the Syncfusion TypeScript Button control, its elements, and more.
platform: TypeScript
control: Overview
documentation: ug
---

# Getting started with Typescript Button

You can create a **TypeScript** application with the help of the given [Typescript Getting Started Documentation](https://help.syncfusion.com/js/typescript).

Create an **HTML** page and add the scripts references in the order, mentioned in the above link Create the **Button** control as follows.

{% highlight html %}

    <body>
    <table>
    <tr>
    <td >My First Button</td>
    <td>
    <input id="button" value="button"/>
    </td>
    </tr>
    </table> 
    </body>


{% endhighlight %}


{% highlight js %}

     ///<reference path="tsfiles/jquery.d.ts" />
     ///<reference path="tsfiles/ej.web.all.d.ts" />
        module ButtonComponent {
            $(function () {
                var sample = new ej.Button($("#button"));
            });
        }

{% endhighlight %}

## Configuring Button Properties

This section encompasses the details on how you can configure the Typescript Button control in your application and customize it with various properties such as various size, resizing the**Button** according to your requirement.

To render the button with required text, size and with rounded corner add the following code example in your TS file.


{%highlight js%}
 
       /// <reference path="tsfiles/jquery.d.ts" />
       /// <reference path="tsfiles/ej.web.all.d.ts" />
        module ButtonComponent {
            $(function () {
                var sample = new ej.Button($("#button"), { text: "Button", showRoundedCorner: true });
            });
        }

{%endhighlight%}


The following screenshot illustrates the **Button** control with text, size and rounded corner properties.



![Button Control in TypeScript](getting-started_images/Getting-Started_img1.JPG)

