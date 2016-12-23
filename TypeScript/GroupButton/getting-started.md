---
layout: post
title: creating a groupbutton in typescript
description: creating a groupbutton in typescript
platform: js
control: Group Button
documentation: ug
---

## Creating a GroupButton in Typescript

You can create a **Typescript** application with the help of the given [https://help.syncfusion.com/js/typescript](https://help.syncfusion.com/js/typescript).In application, Within an index.html file add the scripts references in the order mentioned in the above link.

This can be created from an input element with the HTML id attribute and pre-defined options set to it.

{% highlight html %}
           
            <div class="row">
                <div class="cols-sample-area">
                    <div class="control">
                        <label>Appointment View</label>
                        <div class="element">
                            <div id="GroupButton"></div>
                        </div>
                    </div>
                </div>
            </div>

{% endhighlight %}   
   
Create app.ts file and past the below content

{% highlight javascript %}

    /// <reference path="tsfiles/jquery.d.ts" />
    /// <reference path="tsfiles/ej.web.all.d.ts" />

    module GroupButtonComponent {


    $(function () {
        new ej.GroupButton($("#GroupButton"), {

            dataSource: [

                { text: "Day", contentType: "textonly" },

                { text: "Week", contentType: "textonly" },

                { text: "Work Week", contentType: "textonly" },

                { text: "Month", contentType: "textonly", selected: "selected" },

                { text: "Agenda", contentType: "textonly" }]

        }
        );
    });
        }

{% endhighlight %}

Now build your application, so that the **app.js** is automatically generated and got added to your project (User have nothing to do with this file). Now, whatever code changes that you make in **app.ts** file will be reflected in **app.js** file automatically.


![](creatingagroupbuttonintypescript_images\creatingagroupbuttonintypescript_img1.png)



## Configuring APIs in Group Button

All GroupButton properties, can be configured and used in typescript platform, with types sepcfication. Please refer the below code example to know the configurng the APIs of group button in typescript platform

{% highlight javascript %}

    /// <reference path="tsfiles/jquery.d.ts" />
    /// <reference path="tsfiles/ej.web.all.d.ts" />

    module GroupButtonComponent {


    $(function () {
        new ej.GroupButton($("#GroupButton"), {

            dataSource: [

                { text: "Day", contentType: "textonly" },

                { text: "Week", contentType: "textonly" },

                { text: "Work Week", contentType: "textonly" },

                { text: "Month", contentType: "textonly", selected: "selected" },

                { text: "Agenda", contentType: "textonly" }],
            showRoundedCorner: true,
            selectedItemIndex: [4]           
     
            

        }
        );
    });
        }
        
{% endhighlight %}

The following code will render the following output.

![](configuringapipropertiesingroupbutton_images\configuringapipropertiesingroupbutton_img1.png)


