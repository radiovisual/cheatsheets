#Javascript Cheatsheet

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

##Video

- [Douglas Crockford "Advanced Javascript"](http://yuiblog.com/blog/2006/11/27/video-crockford-advjs/)

##Blogs to Follow

- [substack.net](http://substack.net/)
- [davidwalsh.name](http://davidwalsh.name/)
- [javascriptissexy.com](http://javascriptissexy.com/)
- [②ality – JavaScript and more](http://www.2ality.com/2015/03/es6-generators.html)
- [RisingStack Engineering](http://blog.risingstack.com/)

##Noteworthy Articles

- [Understand JavaScript Closures With Ease](http://javascriptissexy.com/understand-javascript-closures-with-ease/)
- [JavaScript Objects in Detail](http://javascriptissexy.com/javascript-objects-in-detail/)
- [Understand JavaScript’s “this” With Clarity, and Master It](http://javascriptissexy.com/understand-javascripts-this-with-clarity-and-master-it/)
- [Beautiful JavaScript: Easily Create Chainable (Cascading) Methods for Expressiveness](http://javascriptissexy.com/beautiful-javascript-easily-create-chainable-cascading-methods-for-expressiveness/)
- [JavaScript’s Apply, Call, and Bind Methods are Essential for JavaScript Professionals](http://javascriptissexy.com/javascript-apply-call-and-bind-methods-are-essential-for-javascript-professionals/)
