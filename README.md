This is a mirror of https://loufranco.com/github

Here is an overview of my open source contributions in GitHub

## Page-o-Mat

In August of 2022, I published Page-o-Mat.

Page-o-Mat is a python program that can generate custom journals as a PDF. The journal is specified as YAML file with a few options on paper and page template styles. 

Page blocks can be specified in nested "loops" and the loop indices are available to calculate dates (with simple expressions) that can be used as titles on the pages. This allows you to easily create a daily journal, but also allows for more complex journal styles.

A complete example that implements a "[recurring journal](https://loufranco.com/blog/recurring-journals)" is provided.

## Net Worth Estimator

In May 2021, I wrote a few blog posts about personal finance and modeling the effect of savings on net worth growth.

* [My first lesson in personal finance](https://loufranco.com/blog/the-day-i-learned-about-personal-finance)
* [Net Worth Estimator Spreadsheet](https://loufranco.com/blog/very-simple-net-worth-estimator)
* [Net Worth Estimator Spreadsheet Documentation](https://loufranco.com/blog/the-net-worth-spreadsheet-documentation)
* [Net Worth Estimator Spreadsheet in Python](https://loufranco.com/blog/convert-net-worth-spreadsheet-to-vanilla-python)

[I put the spreadsheet and a python port in GitHub](https://github.com/loufranco/net-worth-estimator).

## NerdSummit 2021

In March 2021, I updated the [NerdSummit app](https://github.com/app-o-mat/NerdSummit). I added support for Dark Mode, and since the event will be virtual, I added a button to the session screen to join remotely.

## App-o-Mat iOS Apps

In July 2020, I decided to open-source some of my iOS Apps.

*   [GameOMatKit](https://github.com/app-o-mat/GameOMatKit) : A Swift Package for making one/two-player pong-like educational games.
*   [Math-o-Mat](https://github.com/app-o-mat/MathOMat) : An iOS game made with GameOMatKit that helps you practice arithmetic.
*   [Cap-o-Mat](https://github.com/app-o-mat/CapOMat) : An iOS game made with GameOMatKit that helps you practice US state capitals.
*   [3D-o-Mat](https://github.com/app-o-mat/3DOMat) : An iOS app that can combine two images (left and right eye) into a 3D photo that you can see with red/cyan 3D glasses.

## Bicycle

Bicycle is a datastructure and algorithm that is like a spreadsheet but supports multiple functions per cell and circular references as long as all of the functions are consistent with each other. It will propagate based on whatever values you seed it with.

Read more in [What is Bicycle?](https://loufranco.com/blog/what-is-bicycle)

There are versions in [Swift](https://github.com/spheresoftinc/SwiftBicycle) and [TypeScript](https://github.com/spheresoftinc/bicycle-network).

## NerdSummit 2020

In January 2020, I updated the [NerdSummit app](https://github.com/app-o-mat/NerdSummit). It now uses Google Sheets to provide the schedule and sponsor data, and you can search by author.

## Simple Heatmap Visualization in Alamode

In October 2019, I wanted to show a Mode analytics report as a heatmap. Mode maintains an [open-source gallery of visualizations](https://mode.com/example-gallery), but the only heatmap was specific to cohort retention visualizations. So, I started from that and created a simple generic heatmap that can be used for any two-label data in Mode.

[https://github.com/mode/alamode/pull/42](https://github.com/mode/alamode/pull/42)

It has been merged and you can get it from the normal mode deployment.  To use in a report, edit the HTML and add

    <link rel="stylesheet" href="https://mode.github.io/alamode/alamode.min.css">
    <script src="https://cdnjs.cloudflare.com/ajax/libs/moment.js/2.17.1/moment.min.js"></script>
    <script src="https://mode.github.io/alamode/alamode.min.js"></script>

Then, create an element in your code where you want the heatmap. For example:

    <div id="heatmap" class="col-md-12"></div>

And call the simpleHeatmap function like this (I am using it to track test coverage of iOS devices):

    <script>
    alamode.simpleHeatmap(
    {
        query_name: "Coverage",
        html_element: "#heatmap",
        x_column: "area",
        y_column: "device_and_os",
        value_column: "evnormalized",
        max_value: 100,
        min_value: 0,

        title: "Coverage for 2019.13",
        x_label: "Area",
        y_label: "Device / OS",
        value_is_percent: false,
        color_gradient: ["#d73027","#f46d43","#fdae61","#fee08b","#ffffbf","#d9ef8b","#a6d96a","#66bd63","#1a9850"]
    }
    )
    </script>

## Trello iOS Assisted Onboarding

I work on Trello’s iOS apps. In 2019, I worked on a project to implement an assisted onboarding experience for our apps that supports accessibility, localization, size adaptation and is written in a pure Rx-MVVM style that results in a declarative ViewController and a stateless ViewModel. We open-sourced the VC/VM and unit tests in a sample app.

[https://github.com/trello/trello-ios-assisted-onboarding](https://github.com/trello/trello-ios-assisted-onboarding)

In July of 2019, [I spoke about this project at SwiftFest](http://loufranco.com/rx-presentation).

## Surge

I added [eigenDecompose and unit-tests](https://github.com/Jounce/Surge/pull/95) to Surge in February 2019.

> Surge is a Swift library that uses the Accelerate framework to provide high-performance functions for matrix math, digital signal processing, and image manipulation.

## ListOMat Update / Skillshare course

In January 2019 I added some [branches to ListOMat](https://github.com/app-o-mat/ListOMat/tree/skillshare-starting-point)  and broke down step-by-step instructions for SiriKit to augment my [Skillshare course on SiriKit](https://github.com/app-o-mat/ListOMat/tree/skillshare-starting-point).

## NerdSummit 2019

In January 2019, I updated the [NerdSummit app](https://github.com/app-o-mat/NerdSummit). It now has server customizable session tracks, a slightly better session view, and the sponsor page is fed with server-side JSON.

## Bluepill

In October 2018, I added a feature to [bluepill](https://github.com/linkedin/bluepill) to support my work at Trello. Bluepill is a project that makes iOS GUI Testing easier by orchestrating the simulators and tests. My feature allows [bluepill to call user scripts](https://github.com/linkedin/bluepill/pull/290) after it boots a simulator, but before the test is run. In my use-case, this allows me to install HTTPS certificates into the simulator so that it can connect to our mocked server setup.

## Smashing Magazine 2018

In April 2018, I wrote an article titled [Will SiriKit’s Intents Fit Your App? If So, Here’s How To Use Them](https://www.smashingmagazine.com/2018/04/sirikit-intents-app-guide/). The source code for a simple to-do app with Siri support is here:

[https://github.com/app-o-mat/ListOMat](https://github.com/app-o-mat/ListOMat)

In June 2018, I covered [WWDC 2018](https://www.smashingmagazine.com/2018/06/wwdc-2018-diary-ios-developer/). To explain Siri Shortcuts, I added support to List-o-Mat and put it in a branch.

[https://github.com/app-o-mat/ListOMat/tree/xcode-10-custom-siri-intents](https://github.com/app-o-mat/ListOMat/tree/xcode-10-custom-siri-intents)

## Fastlane

In March 2018, I made a minor commit to fix a bug in how fastlane parses workspaces (via Cocoapods’s Xcodeproj), and I wrote up a [case study about it on App-o-Mat](https://app-o-mat.com/post/how-to-contribute-to-fastlane).

## NerdSummit 2018

In March 2018, I updated the [NerdSummit app](https://github.com/app-o-mat/NerdSummit) (which I forked from my EventOMat). The main feature was to load the schedule from their website instead of including it in the app.

## Smashing Magazine 2017

In April 2017, I wrote an article titled [Simplifying iOS Game Logic With Apple’s GameplayKit’s Rule Systems](https://www.smashingmagazine.com/2017/04/ios-game-logic-gameplaykit/). The source code is here:

[https://github.com/loufranco/PuzOMatPlayground](https://github.com/loufranco/PuzOMatPlayground)

In May 2017, I wrote an article titled [Building Killer Robots: Game Behavior In iOS With Fuzzy Logic Rule Systems](https://www.smashingmagazine.com/2017/05/robots-game-ios-fuzzy-logic/). The source code is here:

[https://github.com/loufranco/FuzzyLogicPlayground](https://github.com/loufranco/FuzzyLogicPlayground)

In July 2017, I wrote a summary of WWDC 2017 with code samples. The Face Detector app from that article is here:

[https://github.com/loufranco/FaceDetector](https://github.com/loufranco/FaceDetector)

## NerdSummit 2017 / EventOMat

In March 2017, I gave a talk about [practicing iOS development](http://loufranco.com/nerd-summit-ios). As part of that talk, I released [EventOMat](https://github.com/loufranco/EventOMat), a simple app to use to practice app development. It implements a conference app which you could customize for any event.

If you want to use it as a basis for practice, there are exercise branches to checkout which remove a single feature and give overview instructions to help reimplement them.

## iOS Swift Playgrounds

I have released a few projects related to Swift Playgrounds. The details can be found in this post about [how I author iOS Swift Playgrounds](http://loufranco.com/blog/authoring-an-ios-swift-playground-book) and [my presentation about it to iOSDevUK](http://loufranco.com/blog/iosdevuk-lightning-talk-about-swift-playground-books).

*   [PlaygroundSupportMock](https://github.com/loufranco/PlaygroundSupportMock) : a mock version of the PlaygroundSupport framework to use during authoring.
*   [pgbookc](https://github.com/loufranco/pgbookc) : a Playground Book “compiler” that can extract a Contents folder from a host app (used for authoring) and turn it into a .playgroundbook bundle.
*   [ShapeSearch](https://github.com/loufranco/ShapeSearch) : a book I am writing that teaches binary search.

## Talking to the LiveView (bugfix of WWDC talk)

At WWDC 2016, there was a code-sample published along with a talk about how to “talk to the LiveView” of a Swift Playground on iOS. As more iOS10 betas were released (and Swift was updated), this code-sample became out of date. Here is [my fix of TalkingToTheLiveView](https://github.com/loufranco/TalkingToTheLiveView/).

## Hack for Western Mass 2015

On June 6-7, 2015, I participated in the [Hack For Western MA](http://hackforwesternmass.org) on a [project for Gardening the Community](https://github.com/hackforwesternmass/gtcalerts) to help them engage their community and supporters. The project was a pair of native apps (iOS and Android) to send alerts related to volunteer opportunities, events, vegetable availability, and requests for supplies. I built the iOS app and set up Parse integration for push notifications.

## Hack for Western Mass 2014

On June 6-8, 2014, I helped organize the [Hack For Western MA](http://hackforwesternmass.org). I participated on a team that took a Hampshire/Franklin labor study and built visualizations of it. The work for that is here:

[https://github.com/hackforwesternmass/transform-labor](https://github.com/hackforwesternmass/transform-labor)

We used GitHub Pages to deploy it here:

[http://hackforwesternmass.github.io/transform-labor](http://hackforwesternmass.github.io/transform-labor)

It is ongoing work that the Hampshire/Franklin Regional Employment Board and Career Center will help guide.

## Smashing Magazine 2014

In March 2014, I wrote an article for Smashing Magazine, titled [Getting Your App Ready For iOS 7′s New Dynamic Interactions](http://www.smashingmagazine.com/2014/03/17/ios7-new-dynamic-app-interactions/). The source code is here:

[https://github.com/loufranco/DynamicUtility](https://github.com/loufranco/DynamicUtility)

## App-o-Mat: training for cordova and jQueryMobile

In February 2014, I started work on [App-o-Mat](https://app-o-mat.com), which is a tutorial site for jQueryMobile and Cordova. To support that I created a app starter template here:

[https://github.com/app-o-mat/jqm-cordova-template-project](https://github.com/app-o-mat/jqm-cordova-template-project)

## Cordova file plugin pull request

While working for a client on a Cordova problem in June 2014, I found a bug in the file plugin and PR'd a fix:

https://github.com/apache/cordova-plugin-file/pull/55

## Hack for Western Mass 2013

In June 2013, I participated in the Hack For Western Mass, on a team that built a web-based application to manage a distributed seed library. The code is here:

[https://github.com/hackforwesternmass/seednetwork](https://github.com/hackforwesternmass/seednetwork)

The site is deployed in Heroku here:

[http://seednetwork.herokuapp.com](http://seednetwork.herokuapp.com)

## Hello! iOS Development

In 2013, I co-authored a book called [Hello! iOS Development](http://loufranco.com/hello-ios "Hello! iOS"). The source code from the book is here:

[https://github.com/loufranco/hello-ios-source](https://github.com/loufranco/hello-ios-source)
