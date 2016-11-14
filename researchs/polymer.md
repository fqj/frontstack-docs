# Polymer Research

This purpose of this article is analyze the Strengths and Weaknesses of Polymer to compare it with other frameworks/libraries. 

# Table of Contents

* [Analysis](#Analysis)
    1. [Performance](#Performance)
    2. [Browser compatibility](#browser-compatibility)
    3. [Mobile compatibility](#mobile-compatibility)
    4. [Hybrid application](#hybrid-application)
    5. [ES5, ES6 & TypeScript](#es5-es6-typescript)
    7. [Web components](#web-components)
    8. [Security](#security)
    9. [Learning curve](#learning-curve)
    9. [Knowledge needed](#knowledge-needed)
    10. [Stability](#stability)
    11. [Development speed](#development-speed)
    12. [Modules and libraries](#modules-and-libraries)
    13. [Community](#community)
    14. [Latest version](#latest-version)
    15. [Scalability](#scalability)
    16. [Important Projects](#important-projects) 
    17. [Time on the market](#time-on-the-market)
* [Strengths and Weaknesses](#strengths-and-weaknesses) 
* [Conclusion](#conclusion)
* [Table](#table)
* [Sources](#sources)

# Analysis

## Performance

As a sample of the performance difference between 0.5 and 1.0, the results from our medium-list benchmark was that Polymer 1.0 was about 3x faster on Chrome and 4x faster on Safari. The benchmark measures time to first paint for an application with a few thousand nested custom elements, with data binding.

## Browser compatibility

With the polyfills, Polymer works in these browsers:

| Polyfill        | IE10 | IE11+ | Chrome\* | Firefox\* | Safari 7+\* |
|-----------------|------|-------|----------|-----------|-------------|
| Custom Elements | ~    | ✓     | ✓        | ✓         | ✓           |
| HTML Imports    | ~    | ✓     | ✓        | ✓         | ✓           |
| Shadow DOM      | ✓    | ✓     | ✓        | ✓         | ✓           |
| Templates       | ✓    | ✓     | ✓        | ✓         | ✓           |


### Should I use webcomponents-lite.js or webcomponents.js?
We recommend using the webcomponents-lite.js version of the polyfills with Polymer 1.0+. This version is designed to be used with Shady DOM, and does not contain the full Shadow DOM polyfill.

## Shadow DOM v1 and Custom Elements v1
Chrome natively implements the v0 APIs, and work is underway on the v1 APIs.

-   WebKit Nightly has a working implementation of Shadow DOM v1.

-   Edge has on its backlog to support [Shadow DOM v1] and [Custom Elements v1].

-   Firefox currently supports some of the v0 web component APIs behind a flag. Polymer **does not work correctly** with this flag enabled, because of an incompatibility with the web components polyfills.

  [Shadow DOM v1]: https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer/suggestions/6263785-shadow-dom-unprefixed
  [Custom Elements v1]: https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer/suggestions/6261298-custom-elements

Original Source at [https://github.com/webcomponents/webcomponentsjs](https://github.com/webcomponents/webcomponentsjs)
and [https://www.polymer-project.org/1.0/docs/browsers](https://www.polymer-project.org/1.0/docs/browsers)
> To Check browser compatibility of your project here: [https://www.browserstack.com/](https://www.browserstack.com/)

## Mobile compatibility

With the polyfills, Polymer works in these mobile browsers:

| Polyfill        | Chrome Android\* | Safari (iOS 7.1)\* |
|-----------------|------------------|--------------------|
| Custom Elements | ✓                | ✓                  |
| HTML Imports    | ✓                | ✓                  |
| Shadow DOM      | ✓                | ✓                  |
| Templates       | ✓                | ✓                  |

Original Source at [https://github.com/webcomponents/webcomponentsjs](https://github.com/webcomponents/webcomponentsjs)

## Hybrid application

   Polymer.js performance on mobile platforms can often be somewhere between frustrating and problematic:
-   Downloading the entire library and polyfills is slow, and you need to download every Polymer Element that you intend to use.
-   Processing the polyfills, libraries, and custom elements appears to be an expensive task on mobile platforms. Even when the downloading is complete, you still often have a blank screen for a few seconds.
-   Especially for more complex functionality (such as drag-and-drop or rendering into a canvas), you may find that functionality that works fine on the desktop simply does not work properly, or is not yet supported, on the mobile platform.

With Cordova it would be possible to build a hybrid app:

* [Cordova](https://cordova.apache.org/) 
    * Applications execute within wrappers targeted to all the platform relying on WebView to provide the user interface. 
    * Allow the access to native device APIs from the web view.
    * Plugins are an integral part of the cordova huge ecosystem.
    * Documentation [https://cordova.apache.org/docs/en/latest/](https://cordova.apache.org/docs/en/latest/)

Original Source at [https://www.toptal.com/front-end/polymer-js-the-future-of-web-application-development](https://www.toptal.com/front-end/polymer-js-the-future-of-web-application-development)

## PWAs support

Polymer bets heavily on the Progressive Web App as a means to run our webs on mobile.
To make this possible, Polymer uses Polymer App Toolbox.

### Polymer App Toolbox

Polymer App Toolbox is a collection of components, tools and templates for building Progressive Web Apps with Polymer. App Toolbox features:

-   Component-based architecture using Polymer and web components.
-   Responsive design using the [app layout components].
-   Modular routing using the [`<app-route>`] elements.
-   Localization with [`<app-localize-behavior>`].
-   Turnkey support for local storage with [app storage elements].
-   Offline caching as a progressive enhancement, using service workers.
-   Build tooling to support serving your app multiple ways: unbundled for delivery over HTTP/2 with server push, and bundled for delivery over HTTP/1.

  [app layout components]: https://elements.polymer-project.org/elements/app-layout
  [`<app-route>`]: https://elements.polymer-project.org/elements/app-route
  [`<app-localize-behavior>`]: https://elements.polymer-project.org/elements/app-localize-behavior
  [app storage elements]: https://elements.polymer-project.org/elements/app-storage

Original Source at [https://www.polymer-project.org/1.0/toolbox/](https://www.polymer-project.org/1.0/toolbox/)

## ES5, ES6 & TypeScript 

* Pros
    * ES5:
        * You have most browser support.
    * ES6:
        * You have tail call optimization.
        * You have import statements.
        * Lamba's are pretty chill.
        * Immutable and block scoping objects with "const" and "let".
        * Classes and OO inheritence.
        * Functors, and all that functional goodness.
        * String templates that handle interpolation for you.

* Cons
    * ES5:
        * It doesn't have everything that ES6 has.
    * ES6:
        * It doesn't have all the support that ES5 has, but you can always transpile your ES6 code.


## Web components

[Polymer] is a lightweight library that helps you take full advantage of Web Components.

With Web Components, you can create reusable custom elements that interoperate seamlessly with the browser’s built-in elements, or break your app up into right-sized components, making your code cleaner and less expensive to maintain.

[Polymer] sprinkles a bit of sugar over the standard Web Components APIs, making it easier for you to get great results.   

One of the advantages of using web components with Polymer is that it has a built in data binding model (like Angular) enabling complete applications to be made without any other libraries.

[Polymer]: https://www.polymer-project.org/1.0/

## Security  

## Learning curve 

The learning curve for Polymer is measured in hours.  Compared to heavier weight frameworks like ExtJS or Angular, you will sooner be spending your time crafting your application instead of trying to figuring out and fighting with the core of the framework to achieve what you desire.

## Knowledge needed

* Shady Dom, Shadow Dom and Virtual Dom behaviours.
* ES5 or ES6.
* Component design pattern.
* Vulcanize or bundling strategies.

## Stability 

* The Google team is already working on the next version (Polymer version 2). The current version (Polymer version 1) is using v0 Custom Elements. v0 is supported now by Google and Safari only. Custom Elements v1 will be supported by a variety of other browsers including: Microsoft, Opera, Firefox. Developers and businesses can look forward to better performance and the reduced need for Polyfills. This step is huge for the Polymer community.

* Provide smooth migration from Polymer 1.x. To upgrade, you will need to make some changes to your 1.x-based code. These changes are necessitated by both the v0-to-v1 spec transition and a handful of key improvements in Polymer itself.Polymer taken care to limit the number of changes that are strictly required and to ease the process of upgrading.

## Latest version
[Stable Release v1.7.0]

Link to the changeLog [https://github.com/Polymer/polymer/blob/master/CHANGELOG.md]

  [Stable Release v1.7.0]: https://github.com/Polymer/polymer/releases/tag/v1.7.0
  [https://github.com/Polymer/polymer/blob/master/CHANGELOG.md]: https://github.com/Polymer/polymer/blob/master/CHANGELOG.md

## Community 

* Mainly maintained by Google
* Angular community Size in numbers
  * Github Stars 17K
  * Github Forks 4,5K
  * Github Contributors 342
  * Stackoverflow questions 21K
  * Stackoverflow followers 7,7K

## Modules and libraries 

## Development speed  


## Scalability 


## SEO Friendly
### No server-side rendering

Polymer does not support server-side rendering. This results in higher loading times, more HTTP requests and it's not very SEO friendly, since search engines have no way of indexing a page if it's not rendered in the server.

Original Source at [https://www.slant.co/versus/10826/11171/~ionic-framework_vs_polymer](https://www.slant.co/versus/10826/11171/~ionic-framework_vs_polymer)

## Important Projects 

## Time on the market 

# Strengths and Weaknesses 

## Strengths

## Weakness

# Conclusion



# Table

| low |  |  |  | medium |  |  |  | High |
|---|---|---|---|---|---|---|---|---|
| ![](assets/images/1.png) | ![](assets/images/2.png)  | ![](assets/images/3.png) | ![](assets/images/4.png) |  ![](assets/images/5.png)    | ![](assets/images/6.png) | ![](assets/images/7.png) | ![](assets/images/8.png) | ![](assets/images/9.png) |

| Category | Score |
|----------|-------|
| Community | ![](assets/images/1.png) |
| Learning curve | ![](assets/images/1.png) |
| Performance | ![](assets/images/1.png) |
| Browser Compatibility | ![](assets/images/1.png) |
| Mobile Compatibility | ![](assets/images/1.png) |
| ES5 | ![](assets/images/1.png) |
| ES6 | ![](assets/images/1.png) |
| Web components | ![](assets/images/1.png) |
| Reuse components | ![](assets/images/1.png) |
| Security | ![](assets/images/1.png) |
| Time on market | ![](assets/images/1.png) |
| Scalability | ![](assets/images/1.png) |
| Knowledge needed | ![](assets/images/1.png) |
| Development speed | ![](assets/images/1.png) |
| Modules and libraries | ![](assets/images/1.png) |
| Stability | ![](assets/images/1.png) |


## Qualification

| **Polymer** | Qualification | ![](assets/images/1.png) |
|----|------|-----|

> This research has been documented by the resources mentioned above on this document and the FrontStack team can't make test to verify the fully complexity of Polymer and it is based on our own experience.

# Sources

