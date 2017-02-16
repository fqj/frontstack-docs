What's a PWA?

Given as that Google came up with the term, I thought we'd kick off with their definition:

"A Progressive Web App uses modern web capabilities to deliver an app-like user experience."
– Progressive Web Apps
The really exciting thing about PWAs: they could make app development less necessary. Your mobile website becomes your app. Speaking to some of my colleagues at Builtvisible, this seemed to be a point of interesting discussion: do brands need an app and a website, or a PWA?

Fleshing this out a little, this means we'd expect things like push notifications, background sync, the site/app working offline, having a certain look/design to feel like a native application, and being able to be set on the device home screen.

These are things we traditionally haven't had available to us on the web. But thanks to new browsers supporting more and more of the HTML5 spec and advances in JavaScript, we can start to create some of this functionality. On the whole, Progressive Web Apps are:

Progressive
Work for every user, regardless of browser choice because they're built with progressive enhancement as a core tenet.
Responsive
Fit any form factor: desktop, mobile, tablet, or whatever is next.
Connectivity independent
Enhanced with service workers to work offline or on low quality networks.
App-like
Feel like an app to the user with app-style interactions and navigation because they're built on the app shell model.
Fresh
Always up-to-date thanks to the service worker update process.
Safe
Served via HTTPS to prevent snooping and ensure content hasn't been tampered with.
Discoverable
Are identifiable as "applications" thanks to W3C manifests and service worker registration scope allowing search engines to find them.
Re-engageable
Make re-engagement easy through features like push notifications.
Installable
Allow users to "keep" apps they find most useful on their home screen without the hassle of an app store.

Linkable
Easily share via URL and not require complex installation.
Source: Your First Progressive Web App (Google)
It's worth taking a moment to unpack the "app-like" part of that. Fundamentally, there are two parts to a PWA: service workers (which we'll come to in a minute), and application shell architecture. Google defines this as:

...the minimal HTML, CSS, and JavaScript powering a user interface. The application shell should:
load fast
be cached
dynamically display content
An application shell is the secret to reliably good performance. Think of your app's shell like the bundle of code you'd publish to an app store if you were building a native app. It's the load needed to get off the ground, but might not be the whole story. It keeps your UI local and pulls in content dynamically through an API.
– Instant Loading Web Apps with an Application Shell Architecture
This method of loading content allows for incredibly fast perceived speed. We are able to get something that looks like our site in front of a user almost instantly, just without any content. The page will then go and fetch the content and all's well. Obviously, if we actually did things this way in the real world, we'd run in to SEO issues pretty quickly, but we'll address that later too.

If then, at their core, a Progressive Web App is just a website served in a clever way with extra features for loading stuff, why would we want one?

The use case

Let me be clear before I get into this: for most people, a PWA is something you don't need. That's important enough that it bares repeating, so I'll repeat it:

You probably don't need a PWA.

The reason for this is that most websites don't need to be able to behave like an app. This isn't to say that there's no benefit to having the things that PWA functionality can bring, but for many sites, the benefits don't outweigh the time it takes to implement the functionality at the moment.

When should you look at a PWA then? Well, let's look at a checklist of things that may indicate that you do need one...

Signs a PWA may be appropriate

You have:

Content that regularly updates, such as stock tickers, rapidly changing prices or inventory levels, or other real-time data
A chat or comms platform, requiring real-time updates and push notifications for new items coming in
An audience likely to pull data and then browse it offline, such as a news app or a blog publishing many articles a day
A site with regularly updated content which users may check in to several times a day
Users who are mostly using a supported browser
In short, you have something beyond a normal website, with interactive or time-sensitive components, or rapidly released or updated content. A good example is the Google Weather PWA:


If you're running a normal site, with a blog that maybe updates every day or two, or even less frequently, then whilst it might be nice to have a site that acts as a PWA, there's probably more useful things you can be doing with your time for your business.

How they work

So, you have something that would benefit from this sort of functionality, but need to know how these things work. Welcome to the wonder that is the service worker.

Service workers can be thought of as a proxy that sits between your website and the browser. It calls for intercept of things you ask the browser to do, and hijacking of the responses given back. That means we can do things like, for example, hold a copy of data requested, so when it's asked for again, we can serve it straight back (this is called caching). This means we can fetch data once, then replay it a thousand times without having to fetch it again. Think of it like a musician recording an album — it means they don't have to play a concert every time you want to listen to their music. Same thing, but with network data.

If you want a more thorough explanation of service workers, check out this moderately technical talk given by Jake Archibald from Google.



What service workers can do

Service workers fundamentally exist to deliver extra features, which have not been available to browsers until now. These includes things like:

Push notifications, for telling a user that something has happened, such as receiving a new message, or that the page they're viewing has been updated
Background sync, for updating data while a user isn't using the page/site
Offline caching, to allow a for an experience where a user still may be able to access some functionality of a site while offline
Handling geolocation or other device hardware-querying data (such as device gyrpscope data)
Pre-fetching data a user will soon require, such as images further down a page
It's planned that in the future, they'll be able to do even more than they currently can. For now though, these are the sorts of features you'll be able to make use of. Obviously these mostly load data via AJAX, once the app is already loaded.

What are the SEO implications?

So you're sold on Progressive Web Apps. But if you create one, how will you make sure it ranks? As with any new front-end technology, there are always implications for your SEO visibility. But don't panic; the potential issues you'll encounter with a PWA have been solved before by SEOs who have worked on JavaScript-heavy websites. For a primer on that, take a look at this article on JS SEO.

There are a few issues you may encounter if you're going to have a site that makes use of application shell architecture. Firstly, it's pretty much required that you're going to be using some form of JS framework or view library, like Angular or React. If this is the case, you're going to want to take a look at some Angular.JS or React SEO advice. If you're using something else, the short version is you'll need to be pre-rendering pages on the server, then picking up with your application when it's loaded. This enables you to have all the good things these tools give you, whilst also serving something Google et al can understand. Despite their recent advice that they're getting good at rendering this sort of application, we still see plenty of examples in the wild of them flailing horribly when they crawl heavy JS stuff.

Assuming you're in the world of clever JS front-end technologies, to make sure you do things the PWA way, you'll also need to be delivering the CSS and JS required to make the page work along with the HTML. Not just including script tags with the <code>src attribute, but the whole file, inline.

Obviously, this means you're going to increase the size of the page you're sending down the wire, but it has the upside of meaning that the page will load instantly. More than that, though, with all the JS (required for pick-up) and CSS (required to make sense of the design) delivered immediately, the browser will be able to render your content and deliver something that looks correct and works straightaway.

Again, as we're going to be using service workers to cache content once it's arrived, this shouldn't have too much of an impact. We can also cache all the CSS and JS external files required separately, and load them from the cache store rather than fetching them every time. This does make it very slightly more likely that the PWA will fail on the first time that a user tries to request your site, but you can still handle this case gracefully with an error message or default content, and re-try on the next page view.

There are other potential issues people can run in to, as well. The Washington Post, for example, built a PWA version of their site, but it only works on a mobile device. Obviously, that means the site can be crawled nicely by Google's mobile bots, but not the desktop ones. It's important to respect the P part of the acronym — the website should enable features that a user can make use of, but still work in a normal manner for those who are using browsers that don't support them. It's about enhancing functionality progressively, not demanding that people upgrade their browser.

The only slightly tricky thing with all of this is that it requires that, for best experience, you design your application for offline-first experiences. How that's done is referenced in Jake's talk above. The only issue with going down that route: you're only serving content once someone's arrived at your site and waited long enough to load everything. Obviously, in the case of Google, that's not going to work well. So here's what I'd suggest...

Rather than just sending your application shell, and then using AJAX to request content on load, and then picking up, use this workflow instead:

User arrives at site
Site sends back the application shell (the minimum HTML, JS, and CSS to make everything work immediately), along with...
...the content AJAX response, pre-loaded as state for the application
The application loads that immediately, and then picks up the front end.
Adding in the data required means that, on load, we don't have to make an AJAX call to get the initial data required. Instead, we can bundle that in too, so we get something that can render content instantly as well.

As an example of this, let's think of a weather app. Now, the basic model would be that we send the user all the content to show a basic version of our app, but not the data to say what the weather is. In this modified version, we also send along what today's weather is, but for any subsequent data request, we then go to the server with an AJAX call.

This means we still deliver content that Google et al can index, without possible issues from our AJAX calls failing. From Google and the user's perspective, we're just delivering a very high-performance initial load, then registering service workers to give faster experiences for every subsequent page and possibly extra functionality. In the case of a weather app, that might mean pre-fetching tomorrow's weather each day at midnight, or notifying the user if it's going to rain, for example.

Going further

If you're interested in learning more about PWAs, I highly recommend reading this guide to PWAs by Addy Osmani (a Google Chrome engineer), and then putting together a very basic working example, like the train one Jake mentions in his YouTube talk referenced earlier. If you're interested in that, I recommend Jake's Udacity course on creating a PWA available here.

