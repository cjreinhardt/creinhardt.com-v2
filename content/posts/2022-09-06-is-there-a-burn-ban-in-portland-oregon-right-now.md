---
title: Is there a burn ban in Portland, Oregon right now?
date: 2022-09-06T03:27:13.712Z
tags:
  - netlify
  - portland
  - oregon
  - javascript
  - html
  - serverless
  - functions
categories: projects
description: null
cover:
  hidden: false
  relative: false
  image: /images/uploads/socialcard.jpg
  alt: The text 'PDX' with a 'fire' emoji, followed by an X and a question mark.
editPost:
  URL: https://github.com/cjreinhardt/PortlandBurnBan
  Text: View on GitHub
  appendFilePath: false
showToc: false
TocOpen: false
comments: false
disableHLJS: false
disableShare: false
hideSummary: false
searchHidden: false
ShowReadingTime: false
ShowBreadCrumbs: false
ShowPostNavLinks: false
ShowWordCount: false
ShowRssButtonInSectionTermList: false
editost: false
hidemeta: false
UseHugoToc: false
---
We recently got a new fire pit for our backyard, and I wanted to see if there was a burn ban in Portland so we could use it.  Thankfully, Multnomah County has a great page that they update daily with the burn ban status, as well as other fire safety information:  https://www.multco.us/health/staying-healthy/wood-burning-restrictions

However!  I wanted something a little simpler, just a page that tells me if there's a burn ban or not, along with an API endpoint that I can use in a little weather app I was building.  

I've used Netlify for a few projects recently and had been meaning to check out their serverless functions (which I think are AWS Lambda functions in a wrapper).  

Using [Cheerio](https://cheerio.js.org) to scrape the Multnomah County site, I made [this little page](https://portlandburnban.creinhardt.com) that displays 'Yes' or 'No' depending on if there's a burn ban:   Based on previous updates it just looks for the phrase 'mandatory burn ban' in the main content node (#node-37292).  

Is this foolproof? No! But it's just for fun. It's possible i'll add more logic, but for now it works alright.  

You can check out the page here: https://portlandburnban.creinhardt.com\
Source code available here: https://github.com/cjreinhardt/PortlandBurnBan

Cheers!