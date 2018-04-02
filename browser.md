# Browser

> How the browser works

## Reflow

Reflow is the process of recomputing the location of DOM elements _within the "flow"_. A DOM element is within the flow if it does not have `position: absolute;` or `position: fixed;`. One can think about elements in the flow as those elements who position depends on the position of siblings.

Reflow is an expensive operation, and it needs to be performed every time **"something"** happens that affects the flow.
<hr>

A non-exhaustive list of changes that **do** trigger reflow include:

* CSS updates
    * `position` changes
    * `display` changes
    * size changes (e.g. `width`, `height`)
* Removing or adding elements to the DOM
    * It's possible that changes to elements may trigger reflow or both ancestors _and_ descendants
* Changes to a DOM element's text content
* Adding or removing CSS classes from an element

<hr>

A non-exhaustive list of changes that **do not** trigger reflow include:

* CSS updates
    * `transform` changes (these are implemented as shaders)

## References
* [MDN on reflow and other performance subtleties](https://developer.mozilla.org/en-US/Apps/Fundamentals/Performance/App_performance_validation)
* [Chrome on reflow](https://developers.google.com/speed/docs/insights/browser-reflow)
* [Reflows and repaints](http://www.stubbornella.org/content/2009/03/27/reflows-repaints-css-performance-making-your-javascript-slow/)
