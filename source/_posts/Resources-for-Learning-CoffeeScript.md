---
title: Resources for Learning CoffeeScript
date: 2014-04-23 13:01:20
subtitle:
tags:
  - coffeescript
---


## CoffeeScript

CoffeeScript is a little language that compiles into JavaScript. While there is a lot of [debate](https://lostechies.com/bradcarleton/2013/10/23/coffeescript-vs-javascript-dog-eat-dog/) online about the pros and cons of using CoffeeScript, I've decided to just focus on talking about some resources I used to learn this little [loved](https://www.youtube.com/watch?v=RoPnnkYg9nI&gl=US&hl=en) and much [hated](https://ceronman.com/2012/09/17/coffeescript-less-typing-bad-readability/) language.

### Coffee Console - Google Chrome extension

https://chrome.google.com/webstore/detail/coffeeconsole/ladbkfdlnaibelfidknofapbbdlhadfp?hl=en-US *(Free)*

You’ll want to install this Google Chrome extension before getting started. It’s essentially [js2coffee](http://js2.coffee/) in reverse. It compiles CoffeeScript into JavaScript as you type. Another advantage of using the compiler in your browser is that you can quickly pull in other libraries. For example, visiting [Underscore.js](http://underscorejs.org/) allows you to write some Underscore in your CoffeeScript after running it in the console.

![](coffeeconsole-output-in-chrome.jpg)

> See CoffeeScript compiled into JavaScript instantly. After running the code, you can use available libraries in the console.

### The Little Book on CoffeeScript

http://arcturo.github.io/library/coffeescript/ *(Free Online / Paid Paperback)*

I read through this book with my Google Chrome extension open. I took [Alex McCaw](https://twitter.com/maccaw)’s advice and wrote every single line of the book to see how they translate into JavaScript. This book will begin to familiarize you with some essential CoffeeScript syntax (`@` is `this.`, `->` is a function call, `=>` carries over the context of `this` into the function, etc).

### CoffeeScript Docs

http://coffeescript.org/ *(Free)*

The CoffeeScript docs were pretty clear and concise on the specific functionality that CoffeeScript offers and how it translates into JavaScript.

### CoffeeScript Ristretto

https://leanpub.com/coffeescript-ristretto *(Free or Paid)*

This was my favorite CoffeeScript read by far. [Reginald Braithwaite](https://twitter.com/raganwald) taught CoffeeScript to the reader as a new language instead of just translating CoffeeScript into JavaScript. This is the best book for anyone newer to learning JavaScript. It served as a review of the concepts in JavaScript, but skipped the weirdness that is JavaScript (unless that weirdness also existed in CoffeeScript). The book started from the very beginning with values and continued up through classes, closures, and canonicalization. It helped me think of CoffeeScript in it’s own light as opposed to just another layer of translation.

### Other Resources

CoffeeScipt is super simple and can be learned by reading just one of the resources above. Here are some more resources I've encountered that can help you use CoffeeScript to it's fullest potential.

#### More Books / Interative Learning

* ~Essence of CoffeeScript: Syntax Shortcuts - An interative tutorial by Carbon Five that quizzes you as you learn.~ *Link no longer works. There is a repo [here](https://github.com/carbonfive/hi-essence-of-coffeescript) that may be the old tutorial.*

* [Code School: A Sip of CoffeeScript](http://coffeescript.codeschool.com/) - These 6 videos and 36 code challenges cover everything from variables and functions to converting jQuery into CoffeeScript.

* [Smooth CoffeeScript](http://autotelicum.github.io/Smooth-CoffeeScript/) - An introduction to programming in CoffeeScript with an emphasis on clarity and abstraction.

* [CoffeeScript Cookbook](https://coffeescript-cookbook.github.io/) - CoffeeScript recipes for the community by the community.

#### Tools / Guides

* [CoffeeCompile](https://github.com/surjikal/sublime-coffee-compile) - This little Sublime Text plugin is a great way to check what CoffeeScript is compiling into on the fly. I already wrote about it in my [guide to Sublime Text](/a-quick-guide-to-sublime-text).

* [CoffeeScript Style Guide](https://github.com/dsignr/coffeescript-style-guide) - Best-practices and coding conventions for the CoffeeScript programming language.

* [Spectacular](http://abe33.github.io/spectacular/) - Spectacular is a BDD framework for CoffeeScript and JavaScript that attempts to bring the power of RSpec to JavaScript.

* [CoffeeLint](http://www.coffeelint.org/) - CoffeeLint is a style checker that helps keep CoffeeScript code clean and consistent.

#### Blog Posts

* [CoffeeScript Tricks](http://product.hubspot.com/blog/coffeescript-tricks) - Quick blog post covering some tricks that aren't covered in the docs.

* ~JavaScript closures, CoffeeScript do, and dont's - This blog post explains handling closures in CoffeeScript.~ *Link no longer works*

* ~Destructuring CoffeeScript one sip at a time - Destructuring in CoffeeScript is an elegant feature that makes the language feel closer to pure functional languages such as Haskell.~ *Link no longer works*

* [Node with benefits: Using CoffeeScript in your stack](https://medium.com/@sagish/node-with-benefits-using-coffeescript-in-your-stack-e9754bf58668) - Some examples on how to utilize CoffeeScript in a Node environment.

* [CoffeeScript's Existential Operator](http://pewniak747.info/2013/08/24/coffeescripts-existential-operator/) - Using CoffeeScript's existential operator, which helps to remove most null and undefined checks.

* [Some Real World Examples of jQuery and CoffeeScript](http://bleibinha.us/blog/2013/06/some-real-world-examples-of-coffescript-and-jquery) - This post gives a short introduction to CoffeeScript and shows the use of CoffeeScript and jQuery.

* [Module Pattern in JS and CoffeeScript](https://robots.thoughtbot.com/module-pattern-in-javascript-and-coffeescript) - This post looks at the the Module Pattern, pioneered by Douglas Crockford, in both JavaScript and CoffeScript.

* [10 CoffeeScript Feature You Might Not Know](https://jacopretorius.net/2013/05/10-coffeescript-features-you-might-not-know.html) - A few CoffeeScript features that are not that well known.
