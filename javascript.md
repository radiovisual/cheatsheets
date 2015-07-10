#Javascript Cheatsheet


## Standards

- [ECMA-262 6th Edition (ES6)](http://www.ecma-international.org/ecma-262/6.0/)


##Javascript Anti-Patterns

Excerpt from [Learning JavaScript Design Patterns](http://addyosmani.com/resources/essentialjsdesignpatterns/book/#antipatterns)

- Polluting the global namespace by defining a large number of variables in the global context
- Passing strings rather than functions to either `setTimeout` or `setInterval` as this triggers the use of `eval()` internally.
- Modifying the Object class prototype (this is a particularly bad anti-pattern)
- Using JavaScript in an inline form as this is inflexible
- The use of `document.write` where native DOM alternatives such as `document.createElement` are more appropriate. `document.write` has been grossly misused over the years and has quite a few disadvantages including that if it's executed after the page has been loaded it can actually overwrite the page we're on, whilst `document.createElement` does not. We can see here for a live example of this in action. It also doesn't work with XHTML which is another reason opting for more DOM-friendly methods such as `document.createElement` is favorable.

"Knowledge of anti-patterns is critical for success. Once we are able to recognize such anti-patterns, we're able to refactor our code to negate them so that the overall quality of our solutions improves instantly."


##Workshops

- [Cyberwizard Institute Workshops](https://github.com/cyberwizardinstitute/workshops/blob/master/javascript.markdown)

##Advanced Javascript Courses

- [Modern Developer](https://learn.modern-developer.com/)
- [Advanced JS Fundamentals to jQuery & Pure DOM Scripting](https://frontendmasters.com/courses/javascript-jquery-dom/)
- [JavaScript: From Fundamentals to Functional JS](https://frontendmasters.com/courses/js-fundamentals-to-functional/)
- [JS.Next: ES6](https://frontendmasters.com/courses/jsnext-es6/)
- [Hardcore Functional Programming in JavaScript](https://frontendmasters.com/courses/functional-javascript/)
- [Advanced JavaScript](https://frontendmasters.com/courses/advanced-javascript/)
- [Advanced JS: Games & Visualizations](https://www.khanacademy.org/computing/computer-programming/programming-games-visualizations)
- [Syllabus for the Advanced JavaScript class at NYU](https://github.com/advanced-js/syllabus)
- [Advanced Javascript Slides by John Resig](http://ejohn.org/apps/learn/)
- [How to Use ES6 for
   Universal JavaScript Apps](https://medium.com/javascript-scene/how-to-use-es6-for-isomorphic-javascript-apps-2a9c3abe5ea2)


##Video

- [Douglas Crockford "Advanced Javascript"](http://yuiblog.com/blog/2006/11/27/video-crockford-advjs/)
- [Functional Programming with Generators](https://www.youtube.com/watch?v=B2ASp0jb6FY)
- [Hanging Up On Callbacks: Generators in ECMAScript 6](https://www.youtube.com/watch?v=s-BwEk-Y4kg)

##Blogs to Follow

- [substack.net](http://substack.net/)
- [davidwalsh.name](http://davidwalsh.name/)
- [javascriptissexy.com](http://javascriptissexy.com/)
- [②ality – JavaScript and more](http://www.2ality.com/2015/03/es6-generators.html)
- [RisingStack Engineering](http://blog.risingstack.com/)
- [Eric Elliot : Medium](https://medium.com/@_ericelliott)
- [http://ericleads.com/](http://ericleads.com/)

##Noteworthy Articles

- [Understand JavaScript Closures With Ease](http://javascriptissexy.com/understand-javascript-closures-with-ease/)
- [JavaScript Objects in Detail](http://javascriptissexy.com/javascript-objects-in-detail/)
- [Understand JavaScript’s “this” With Clarity, and Master It](http://javascriptissexy.com/understand-javascripts-this-with-clarity-and-master-it/)
- [Beautiful JavaScript: Easily Create Chainable (Cascading) Methods for Expressiveness](http://javascriptissexy.com/beautiful-javascript-easily-create-chainable-cascading-methods-for-expressiveness/)
- [JavaScript’s Apply, Call, and Bind Methods are Essential for JavaScript Professionals](http://javascriptissexy.com/javascript-apply-call-and-bind-methods-are-essential-for-javascript-professionals/)
- [How to Use ES6 for Isomorphic JavaScript Apps](https://medium.com/javascript-scene/how-to-use-es6-for-isomorphic-javascript-apps-2a9c3abe5ea2)
- [Common Misconceptions About Inheritance in JavaScript](https://medium.com/javascript-scene/common-misconceptions-about-inheritance-in-javascript-d5d9bab29b0a)
- [The Dao of Immutability](https://medium.com/javascript-scene/the-dao-of-immutability-9f91a70c88cd)
- [How to Use ES6 for Universal JavaScript Apps](https://medium.com/javascript-scene/how-to-use-es6-for-isomorphic-javascript-apps-2a9c3abe5ea2)
- [Fluent JavaScript – Three Different Kinds Of Prototypal OO](http://ericleads.com/2013/02/fluent-javascript-three-different-kinds-of-prototypal-oo/)
- [Polymorphism That Just Works](http://tobyho.com/2015/06/23/polymorphism-that-just-works/)
- [We have a problem with promises](http://pouchdb.com/2015/05/18/we-have-a-problem-with-promises.html)
- [Anonymous Functions, Assigned To References, Show Up Well In JavaScript Stack Traces](http://www.bennadel.com/blog/2836-anonymous-functions-assigned-to-references-show-up-well-in-javascript-stack-traces.htm?&_=0.32385098887607455)

###General Syntax

**BAD:** var options = options || {};
**GOOD:** [defaults/overrides pattern](https://gist.github.com/ericelliott/f3c2a53a1d4100539f71)

###Style Guides

- [AirBNB JS Styleguide](https://github.com/airbnb/javascript)
