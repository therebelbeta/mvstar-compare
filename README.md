# mvstar-compare

A brief comparison of a few MV* front end frameworks.

## Scope

* Documentation - *How well do they document their API?*
* Learning curve - *How closely does it adhere to current dev standards (how hard is it to learn)?*
* Performance - *How big is it's footprint, and how quickly does it render?*
* Scalability - *How easy is it to scale to potentially enormous factors?*
* Updates - *How often do they update their codebase, and do they introduce API changes often?*
* Testing - *How easy is it to get testing set up?*
* Roadmap - *How supported will this framework be down the line?*
* Backing - *Is this framework being backed by reputable company?*

## Frameworks

* Ember
	* **Pros**
		* Comprehensive toolset of helpers and MVC tools
	* **Cons**
		* Ember's comprehensiveness comes at the cost of a steep learning curve and a high degree of vendor lock-in.
		* Opinionated in terms of how application architecture should look, and as a result, tends to be less transparent in terms of what is actually happening under the hood.
* Angular 1x
	* **Pros**
		* Large community
		* Lots of documentation
		* Backed by google
		* Really fast prototyping
		* Emphasis on testing (with Protractor)
	* **Cons**
		* Roadmap rocky, moving to typescript/es6
		* Not as performant as other frameworks. Steep performance degradation is a notoriously common issue in non-trivial Angular applications and there are several third party libraries which attempt to get around performance problems. Speaking from experience, it's generally difficult to reason about performance in Angular.
		* Implements several subsystems that would seem more logical in programming language implementations (e.g. a parser, a dynamic scoping mechanism, decorators, etc)
	* with the issue of angular 1x getting depricated in 6 months or so, i would hold off on this option.
* React
	* **Pros**
		* fast render
		* Acknowledges that DOM operations are the bottleneck of templating systems, and implements a virtual DOM tree which keeps track of changes and only applies diffs to the real DOM where needed.
		* backed by facebook/instagram
		* very active community
		* very modular / expandable
		* forces developers to think in components
	* **Cons**
		* high learning curve
		* new language?! .jsx
			* JSX syntax does not run natively in the browser
		  * this alone invalidates the myriad of js tools available for testing and syntax highlighting
		* a lot of "magic", unclear at first glance what the library is doing.
		* Only handles the view. Has no built-in methods for controllers, models, routing, ajax calling, anything. Would need to find appropriate libraries for all of these, making it a lengthier time to determine cross-compatibility and prototyping
* [Ampersand](http://ampersandjs.com/)
	* **Pros**
		* VERY clean. Uses Node.js style structuring, making it easy for backend fellows to jump in.
		* Public Trello board to track roadmap and progress of library
		* flexible view/binding model, can even drop in another view library
		* Stemmed from a need for backbone to be more flexible: http://www.infoq.com/news/2014/06/ampersandjs
		* Backed by &yet, a development/consulting company
	* **Cons**
		* [CLI doesn't run in node 0.12 or io.js 1.x](https://github.com/AmpersandJS/ampersand/issues/105)
		* May require an express server... still researching this.
* [Mithril](http://lhorie.github.io/mithril/)
	* https://medium.com/@l1ambda/mithril-vs-angular-vs-react-d0d659c24bae
	* **Pros**
		* Suuuuper small
		* acknowledges that DOM operations are the bottleneck of templating systems, and implements a virtual DOM tree which keeps track of changes and only applies diffs to the real DOM where needed.
		* Faster view rendering than React, without weird jsx compiling, uses DOM-diffing
		* Fasted loading/rendering of all MVC's benched (http://matt-esch.github.io/mercury-perf/)
		* Provides an auto-redrawing system that is aware of network asynchrony and that can render views efficiently without cluttering application code with redraw calls, and without letting the developer unintentionally bleed out of the MVC pattern.
		* Full MVC
		* Easily integrated with other libraries
		* testing is just normal Mocha testing
	* **Cons**
		* looks to be purely open source, no backing company
