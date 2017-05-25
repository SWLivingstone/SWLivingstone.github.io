---
layout: post
title: AngularJS - A High Level View
---

When I first starting learning AngularJS I was fairly new to programming (at the time of writing this I am _still_ fairly new to programming) and had never used a framework before - I only had the vaguest notion of what a framework was.  This meant that a lot of the documentation I read was quite meaningless because it was written with a vocabulary that I did not know.  So, here is my best shot a presenting a high level view of AngularJS for the programming novice.

## Wires and Switches

{:.center}
![]({{ site.baseurl }}/img/wires.jpg)

I like to think of AngularJS as wires and switches.  The wires connect switches together and pass information between the switches.  The switches take information, do something with it, and then return altered information.

If you want to write a complicated app you are going to need many differnt functions (switches) and you are going to have to make sure that each function is sending and receiving its information to and from the right place (the wires help with that part).

The basic conecept of AngularJS as the underlying network of wires and switches behind your app is where this analogy should end.  I simply use this analogy because AngularJS is called a framework and I thought the term to be a bit missleading.  For my own brain's sake it has been better for me to view AngularJS as a flow of information (scopes, variables, etc...) as opposed to a ridged structure holding things up.




## Key Components

{:.center}
![]({{ site.baseurl }}/img/puzzle.ico)

AngularJS supplies for you many tools but to keep things simple we will look at the 4 main components that you will use to build an app.

**Controllers**

_Writen in JavaScript_

These control things.  To stretch the above analogy of wires and switches Controllers are a little bit like wires.  A Controller decides who talks to who and who knows what.  In more technical terms a Controller is responsible for providing a scope.  

In AngularJS we do not rely on a global scope to pass information but instead create local scopes within Controllers.  This way you can control (see why their called controllers?) exactlly which scope a function will be using.

**Services**

_Writen in JavaScript_

A Service is a function or group of functions that perform a specific task (ex: play a song, query a database, etc...).

**Templates**

_Writen in HTML_

Templates are HTML files that make up the View. In AngularJS the View is best thought of as what the user sees.  The view can consist of multiple templates.

With a standard website when a user navigates to a new page a new HTML file is loaded along with any scripts and syle sheets linked to by the new HTML file.  This means that the browser has to reload everything when a new page is navigated to.  In AngularJS the entire app is loaded only once.  When a new page is navigated to a template is simply passed into the view.  This makes for an incredibly responsive user experience.

Also, all DOM manipulation should happen with in Templates.

**Directives**

_Writen in JavaScript_

Directives handle DOM manipulation and are declared within templates.  There are many ready built Directives within AngularJS ([examples](https://www.w3schools.com/angular/angular_directives.asp)) but you can also build your own.


## How Its All Connected

{:.center}
![]({{ site.baseurl }}/img/dataFlow.png)

The above image shows the flow of information in AngularJS.  Each Template is assigned a Controller.  Whenever a Template needs to do something (such as calling a function or using a variable) it talks to its Controller.  The Controller then talks to whatever Service it has been injected with (a common term in AngularJS for connecting Services, Controllers, Templates, and Directives is injection).  The Service _does something_ using its own local variables as well as variables provided by the Controller - this is known as the scope.  The Controller also has access to variables from the Template which it can then pass onto the Service.  When the Service is done _doing something_ it then passes it to the Controller which passes it to the Template.

Now, that all may seem pretty unnecessary, and for a small program it is, but when a program is large and complicated it is invaluable.  You can inject any number of Services you wish into a single Controller and you can inject a single Service into as many Controllers as you wish.  This means that one Service can work for a dozen different Controllers and Templates using a dozen different scopes for its variables.  You can also mix and match Services injecting them only into the Controllers that need them.  Now your program is modular ([Separation of Concerns](https://en.wikipedia.org/wiki/Separation_of_concerns)).

Directives are a little more straight forward.  They talk Directly with the template that they have been declared in.  By declared I mean literally writen into the HTML like this.
```
<ng-somedirective></ng-somedirective>

<div ng-directive = "somefunction()">
</div>
```
You can declare a single Directive in as many Templates as you wish and you can declare as many different Directives in a single Template as you wish.

## The Wrap Up

That is how I see AngularJS from a high level perspective.  If you think that any of what I have written is inaccurate or I was wrong about something - I probably was - please send me an email (ScottWLivingstone@gmail.com) and let me know how I can make this article better.


**A quick diagram to show an effective way to organize your files when using AngularJS**

{:.center}
![]({{ site.baseurl }}/img/fileTree.png)
