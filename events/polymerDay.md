# Polymer Day

![](assets/polymer_day.png)

## Introduction
The main purpose of this document is to share topics and keywords that appeared in PolymerDay.

## Polymer 2
Polymer 2 was presented early next year and this is what they told us:

* Support to Polymer 1.0.
* Hybrid mode, to ease the migration from Polymer v1.0 to Polymer v2.0
* Extend components. A very useful utility that so far in Polymer 1.0 was not possible, and opens new avenues for reuse of code.

* Preview Polymer v2.0 [https://www.polymer-project.org/1.0/blog/2016-09-09-polymer-2.0](https://www.polymer-project.org/1.0/blog/2016-09-09-polymer-2.0)
    * This new versión mainly take advantage of native v1 Shadow DOM and v1 Custom Elements API’s with the commitment to be implemented by all the major browsers.
     
* Evolution to EcmaScript 6 and in particular the use of classes.
* Certain options offered by the web platform itself are used, so certain abstractions disappear.
* Adaptation to the specification "v1" Shadow DOM and Custom Elements.

## Polymer Style guides
[http://polymerelements.github.io/style-guide/](http://polymerelements.github.io/style-guide/)

# Event Schedule

## Polymer: How we got here and where we're going

* Speaker: Taylor Savage - https://twitter.com/taylorthesavage

An overview of the Polymer project and Web Components, and our vision for the future.
Taylor Savage announced who already using Polymer in their applications: Google Chrome, YouTube, Google Play Music and many more.<br>
They also said companies like USA Today, BBVA, ING, Net-a-Porter, Coca-Cola and Predix.<br>
This is just a sample of what is being implemented with Polymer, which can be complemented with projects published:

* Built with Polymer [https://www.polymer-project.org/1.0/blog/2016-09-09-polymer-2.0](https://builtwithpolymer.org/)
* Polymer Who's using? [https://github.com/Polymer/polymer/wiki/Who's-using-Polymer%3F](https://github.com/Polymer/polymer/wiki/Who's-using-Polymer%3F)

## Polymer 2.0: Under the hood 

* Speaker: Rob Dodson - https://robdodson.me/ - https://twitter.com/rob_dodson

It's not always clear to developers the boundaries between native web components and Polymer. What does the library add? What's already built into the platform? This talk aims to demystify Polymer by peeling back the cover to explain how the internals work and show how they complement existing APIs. We'll cover the basics of building vanilla web components using the new v1 specs, and demonstrate new features in Polymer 2.0 that make the whole process more efficient.

More info in his channel:
* [https://www.youtube.com/playlist?list=PLOU2XLYxmsII5c3Mgw6fNYCzaWrsM3sMN](https://www.youtube.com/playlist?list=PLOU2XLYxmsII5c3Mgw6fNYCzaWrsM3sMN)

## Polymer for StartUps

* Speaker: Victor Sánchez - https://www.linkedin.com/in/victorsanchezbelmar - https://twitter.com/VictorSanchez

Web components and polymer change the way we work and think in our startup, in this talk we would give you and overview on how polymer improved our workflow what features we use and love and how it can change your startup too.

Victor Sánchez explained his experience as a SyncRTC CEO ([www.syncrtc.com](https://www.syncrtc.com/landing/index.html)) and how Web Components help them to grow and agile evolution.   
He also explain his current project [#IEWOWRoom](http://www.ie.edu/madeofchange/), an IE innovative video conference platform.
Some impressive details:
* 15 meter long screen, 45 square meters and 48 screens.
* Students emotion detection.
* Realtime interaction such as polls, questions, etc.
* Realtime Big data visualization 
* Visual interface built with Polymer Components.

For more info: 
 * [http://es.euronews.com/2016/10/21/ie-business-school-lanza-un-proyecto-educativo-unico-en-europa-iewowroom](http://es.euronews.com/2016/10/21/ie-business-school-lanza-un-proyecto-educativo-unico-en-europa-iewowroom)
 * [http://cincodias.com/cincodias/2016/10/20/tecnologia/1476972071_876168.html](http://cincodias.com/cincodias/2016/10/20/tecnologia/1476972071_876168.html)

## Building Components for Business Apps

* Speaker: Manolo Carrasco Moñino - https://www.linkedin.com/in/manolocarrasco - https://twitter.com/dodotis

Web components and Progressive Web App technologies offer a solution to fragmented development and runtime environments by allowing you to reuse code between both: frameworks and platforms. Vaadin works simplifies the development of business apps by providing UI components and tools that are focused on helping business app developers.

The Vaadin component [angular2-polymer](https://github.com/vaadin/angular2-polymer) simplify the integration Angular2 with Polymer and avoid known boilerplates.  

Polymer Component Catalog 
* [beta.webcomponents.org](beta.webcomponents.org)
* [Vaadin elements](vaadin.com/elements)

## Polymer in large projects: Advantages and Disadvantages

* Speakers: 
    * Rafa García - https://www.linkedin.com/in/rafaelgarciasimon - https://twitter.com/rafagarcia
    * Jon Rojí - https://www.linkedin.com/in/jonroji

## Creating a template for Polymer CLI

* Speaker: Abdón Rodríguez Davila - https://abdonrd.com/ - https://www.linkedin.com/in/abdonrd - https://twitter.com/abdonrd

Polymer CLI is a command line interface for Polymer projects. Abdon showed us how to create your own template for it. Run a command to create a custom skeleton to be ready to start something new. 

* How to build
    * App Shell with service worker to load fast the project structure.

* What is App Shell?
    * App shell means something like the minimum structure of our project where we will load other components. The idea is to minimize the impact load web components.

* Modules for mounting a starter kit of Polymer
    * [Polymer-build](https://github.com/Polymer/polymer-build) to build the Polymer App.
    * [Polymer-analizer](https://github.com/Polymer/polymer-analyzer) better than Hidrolic for Linting

## Polymer better with Angular 2

*  Speaker: Rubén Aguilera - https://twitter.com/raguilera82

Ruben Aguilera, explained on a shoestring how to integrate Polymer with Angular2 natively without the need to integrate third-party plugins, giving rise to an architecture in which the work of developers and designers is clearly defined time.

The integration of Angular2 Framework and Polymer components require:
* Angular2 communicates with Polymer through attribute binding.
* Polymer interacts with Angular2 through event triggers.

Resources:
* Video explaining how to integrate both [https://www.youtube.com/watch?v=brna1jy0kZQ](https://www.youtube.com/watch?v=brna1jy0kZQ)
* Article about the integration [https://www.adictosaltrabajo.com/tutoriales/integracion-de-angular-2-con-polymer/](https://www.adictosaltrabajo.com/tutoriales/integracion-de-angular-2-con-polymer/)

## Improve your app performance

* Speaker: Eduardo Sada - https://es.linkedin.com/in/eduardosada - https://twitter.com/aeroalquimia

Eduardo talked us about techniques to improve the performance of web applications progressive.
When creating an application we must keep in mind to which device is oriented. The problem is that today mobile is no longer an option, the trend is mobile first.

@aeroalquimia was spectacular telling his experience with the performance of their applications.

First he told us that he had many problems with the visual experience of its developments in mobile as it did not match what he saw in your browser. This basically was because the developed on a macbook with a enormous power and then tested in a development nexus 3 or 4. The result was disastrous, and his first thought was to emulate the performance of your mobile in the browser. He made a benchmark on his computer and one on the mobile phone using this tool: [Motion Mark](http://browserbench.org/MotionMark/)
The result obtained was that his performance is 200 of score and on mobile approx 20 score. With this difference of x10 slower, he went to Chrome Canary and applied a reduction -x10 his pc to simulate the gpu.
It is also possible in Chrome Canary apply a downgrade of network to simulate environments with little signal.
He talk also about the [RAIL model](https://developers.google.com/web/fundamentals/performance/rail) 

Important notes to keep in mind:
* Mobile first
* [Motion mark](http://browserbench.org/MotionMark/) to measure our performance on PC and mobile
* Chrome Canary for options cpu and network downgrade
* window.performace.mark y window.performance.measure (To measure the parts that interest us, but will not be clear on the network tab)
* [Polydev](https://github.com/PolymerLabs/polydev), polydev is the Polymer DevTools Extension - a tool to help develop Polymer and custom elements.
* Beware with iron-image, it consumes much
* Main Thread. In javascript I can only do One thing at time.
* mobile first: Your laptop is a liar.
* model RAIL:
    * **R**esponse: 100ms (ideales)
        * A simple input takes 20ms
        * Use web workers to work in parallel, but considering that web workers can not modify the dom
    * **A**nimation: 16ms (ideal) 16ms comes from dividing 1 second between the 60 frames.
        * 16ms You can do very little
        * The animation has to be in the main thread
        * If I have remain time then window.requestIdleCallback()
    * **I**dle Work: 50ms chunks
    * **L**oad: 500ms. Do not leave load more than 500ms
* Browser Enemies:
    * Transform: translateZ(0)
    * Polymer.RenderStatus.afternextRender() 
* Trust in the browser
* Chrome guidelines to follow: [WEB FUNDAMENTALS](https://developers.google.com/web/fundamentals/)
* Tool accessibility polymer: Some tools do not work with Shadow DOM
* Channeling pixels

	There are five main areas that should know and consider when working.
	These are areas which have a high level of control, and the key points of channeling pixels to the screen:<br>
	    Javascript -> Style -> Design -> Paint -> Composite<br>
    	A good Frame : Javascript -> Style -> Design -> Paint -> Composite: Total 8ms.

* Optimize the execution of JavaScript

	The synchronized incorrectly or long running JavaScript can be a common cause of performance problems, should try to minimize its impact wherever possible.

	* Avoid using setTimeout or setInterval for visual updates. Instead, always use requestAnimationFrame.
	* Move out of the backbone to the Web Workers long running JavaScript.
	* Use microtask to make changes to the DOM (Document Object Model) in multiple frames.
	* Use the timeline DevTools Chrome and JavaScript profiler to assess the impact of JavaScript.

* Reduce the complexity or use of Web Workers

## Is my application accessible? 

* Speaker: Felix Zapata - https://www.linkedin.com/in/felixzapata - https://twitter.com/felixzapata

Felix Zapata gave us several advices to develop Accessible Websites by using Polymer's web components.
Also he talked about five important rules: <br>
* Alternatives: Alternatives to images, (emoji), and multimedia, mainly.<br>
* Structure: Semantics, structure, data tables, forms, etc.<br>
* Identification: Hide text in an accessible, warn of changes (important), etc.<br>
* Operability: Should i Use a carousel? <br>
* Use of color: Ensure high contrast for text over images and to hell with unreadable, low-contrast texts ! (Contrast Rebellion)<br>

Finally he checked up an application made by Polymer:<br>
   * Shrine template [https://polymerelements.github.io/app-layout/](https://polymerelements.github.io/app-layout/)
And fortunately the mistakes found was not caused by Polymer.

Beware: Some automated review tools do not work very well with the Shadow DOM.

Recommended reading list:<br>
   * Stop Talking About Accessibility [https://envato.com/blog/stop-talking-accessibility-start-talking-inclusive-design/](https://envato.com/blog/stop-talking-accessibility-start-talking-inclusive-design/)<br>
   * Start Talking About [https://envato.com/blog/stop-talking-accessibility-start-talking-inclusive-design/](https://envato.com/blog/stop-talking-accessibility-start-talking-inclusive-design/)

Resources:
* Slides: [https://speakerdeck.com/fzberlinches/es-mi-aplicacion-accesible](https://speakerdeck.com/fzberlinches/es-mi-aplicacion-accesible)
* Pdf: [https://speakerd.s3.amazonaws.com/presentations/b52d2e6ff3764a39a13ad943afee46e1/Es_mi-aplicacion-accesible__-_Polymer-Day.pdf](https://speakerd.s3.amazonaws.com/presentations/b52d2e6ff3764a39a13ad943afee46e1/Es_mi-aplicacion-accesible__-_Polymer-Day.pdf)

## Everyday Polymer

* Speaker: Gloria Bueno - https://es.linkedin.com/in/globits - https://twitter.com/globitss

Gloria Bueno, Google Developer Experts, shared with us some tips on how to work with Polymer on a daily basis and become Polyproductive.

**Yarn** is a manager dependencies like bower or npm, with a promising future.
* Allows offline mode, if you already installed it before, no need to download (implements a cache)
* Npm support packages and bower
* Flat mode
* If the request does not break the installation fails, it will retry later.


## When styles meet Polymer's web components

* Speaker: Zuriñe Menendez Cayrols -  https://www.linkedin.com/in/zurimenendez - https://twitter.com/zmencay

A new age has arrived, an era in which the styles and components go together. Long live the styles and components!

* Slides: [https://dl.dropboxusercontent.com/u/25357006/polymer-day.pdf](https://dl.dropboxusercontent.com/u/25357006/polymer-day.pdf)

## Architectures of web components focus on data

* Speaker: Javier Vélez - https://www.linkedin.com/in/javiervelezreyes - https://twitter.com/javiervelezreye

Most of the applications we handle today correspond to data-centric architectures. Information models exposed as services that are explored in depth. 
In this context, the architectures of Web components are presented as an ideal solution to carry out this exploratory process simple and declaratively. 
Throughout this talk he discussed such architectures and presented fundamental design patterns that meet these types of scenarios.

Resources:
 * Slides about Component oriented Architecture: [http://es.slideshare.net/jvelez77/arquitecturas-para-la-reutilizacin-en-javascript](http://es.slideshare.net/jvelez77/arquitecturas-para-la-reutilizacin-en-javascript)

## Polymer data manager

* Speakers:
    * Pablo Almunia - https://www.linkedin.com/in/pabloalmunia - https://twitter.com/pabloalmunia
    * Wilder Olmos - https://es.linkedin.com/in/wilderolmos - https://twitter.com/wilderolmos

They showed the design and implementation of dynamic configuration of components for system monitoring through data and how it was solved the problem of communication between components using Data Manager unified.
It was showed with examples the approach to componentize the web base on polymer configurable components.


## Offline-First apps with Polymer and PouchDB

* Speakers: Sergio Contreras - https://www.linkedin.com/in/sergiocontrerasmartin - https://twitter.com/sergicontre 

In the current context where everything tends to be portable and can get to use apps in different situations and geographical locations,
it should be able to use common applications despite not be guaranteed connectivity?
In this talk Sergio showed us strategies offline-first (via storage database browser) on applications developed with Web components in Polymer.

This was a very interesting discussion topics. Offline first offers many advantages for end users, which enrich our experience with web applications, where communication with the server is not always needed and of course in scenarios where there isn't a blocking requirement. Offline first allows us to continue using applications without having an internet connection, very useful in inaccessible environments. This in turn requires of technologies as PouchDB among others that what they do is to have a replica of the structure database locally, and allow themselves to be synchronized with the server. These technologies do not define when your app is synchronized, but it does when you want to merge data. Very powerful. This is a paradigm that improves our productivity, utility and user experience. 

Notes:
* PouchDB, CouchDB, IndexedDB
* Allow work anywhere
* The network is not an impediment
* Improves the user experience
* We must create forms of synchronization.

## Polymer and Firebase in action

* Speakers:
    * David Chavarri - https://www.linkedin.com/in/dchavarri - https://twitter.com/dvdchavarri
    * Ruben Chavarri - https://www.linkedin.com/in/ruchavarri - https://twitter.com/pekewake

In the talk Chavarri brothers showed us how to integrate Polymer component and FireBase, the Mobile Backend as a Service platform of Google, Realtime system and Hosting service. 
They also gave us a little introduction to reactive programming, and how to build interactive applications taking advantage of this new approach with Polymer components in our apps to improve the user experience. 
To see all of this in action they ended up developing an interactive application which showed the potential of this awesome synergy Polymer and Firebase, with a collaborative example.

* Slides:  [http://es.slideshare.net/ruchavarri/polymer-and-firebase-in-action](http://es.slideshare.net/ruchavarri/polymer-and-firebase-in-action)

# Polymer Day Pictures

* [https://photos.google.com/share/AF1QipNNhjs4u69HlIvr6zI3LbEW8Z9OZ6IWah1ebxXsV8lyLrQ0MiI1r6D4PTXhCXc3Nw?key=SzJObU9aZW1oeFVVbGxPZm1vMGo2d1d2aDdsanFR](https://photos.google.com/share/AF1QipNNhjs4u69HlIvr6zI3LbEW8Z9OZ6IWah1ebxXsV8lyLrQ0MiI1r6D4PTXhCXc3Nw?key=SzJObU9aZW1oeFVVbGxPZm1vMGo2d1d2aDdsanFR)
