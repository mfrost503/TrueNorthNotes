# Practical Software Design
# Adrian Schneider @AdrianSchneider

## Perspective
* Learn from failing
* Failure dictates how we build software
* We are all biased
* Stay motivated
* Our industry is nuts
* Don't be the smartest one in the room
* Look for sources of inspirations

## Poor Design
* We can all recognize bad design
* We don't intentionally create bad software
* Business don't want bad software
* Somehow it still happens
* Caching is a band-aid
* Hurts developer morale
* Unsustainable
* People give up

## Solutions
* We are hired to solve business problems
* Reality is constrained
* Some change or can change
* Challenge the constraints
* Find balance - when do I fight and when do I incur debt
* Businesses care about money, learn to speak it
* Rewrites are expensive
## Foundation
* Architecture is foundation
* Larger the scope, the wider base we need
* Know the shelf-life and build to support it
* Requirements - is the spec final, will it change into something else?
* we assume it won't change and it does and we get mad
* Team composition - 3000 workers vs 5 highly-skilled workers

## Frameworks
* Many problems we face are already solved
* Full stack is like working at big company with it's own way of doing things
* Rapid Application Development (RAD) heavily lean on conventions
* Micro - lightweight base with few assumptions
* Libraries provide sane abstractions over common problems
* Ideally we can swap them
* Compose rather than extend

## Feedback
* Tight feedback loops allows us to go much faster
* a slow one will kill projects
* No feedback - ignorant, unknowingly creates debt
* Fixing bugs years/months later is really expensive
* Delayed feedback - requires a context switch to act on
* Slow - blocking or throttling, knowingly creating debt
* Instant feedback - No external delays, no experimentation costs
* Methods - good ways and bad ways to test
	* Refresh
	* Have QA test it
	* Wait until CI runs
	* Unit tests
* Tightening the loop
* Automatically test on save
* Reduce the individual test scope
* Cut extraneous IO
* Leaning on tools for new feedback.
* Tight feedback is magical
* Simulate anticipate failure
* Foundation can be iterative
* Experiment quickly and safely

## Designing Better Software
* Better software is simpler software
* Goal is to always simplify
* Domain modeling
	* Don't just dive in
	* More code won't fix the wrong design
* Modeling Reality
	* Model is a small representation
	* Iterative, just like your code
	* Teams, relations, processes, workflows
* Book: Domain Driven Design
	* Build model in isolation
	* Everything else is in the implementation detail
	* Don't deviate from the model
* Entities are things
* Value Object are immutable, shouldn't change, just be assigned differently
* The Unix Philosophy
* Write programs that do one thing and do it well
* Write programs that work together
* Write programs that handle text streams
* Because that is a universal interface
* Compose applications from smaller units
* Boundaries
	* Find sub-systems
	* Minimize their surface area
	* Horizontal components
	* Vertical Layers
* Build domain separately and test that
* Be more conscious and consistent with design efforts
* Better software is the result.
* Continuous Improvement for continued sanity
* Master your tools and feedback cycle
* Solve problems
* Most code problems are design problems
