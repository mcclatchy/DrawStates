#DrawStates

DrawStates is a plugin for [Raphael](http://raphaeljs.com/) designed to produce a simple map of all US states which can be quickly embedded into HTML content. The plugin uses a predefined project of the US to render 52 polygons, one for each state and blocks each to represent national data and the District of Columbia.

The initial map is drawn by calling the `drawStates()` function, which takes a single parameter -- either a string representing the ID attribute of the HTML node to insert the map or the DOM node itself.

Each state is drawn as a single Raphael path, and can have any attributes or interactivity available to Raphael applied to it. The output map is then scaled down to the size of the size of its container node, keeping an aspect ratio of 1.5, and a jQuery listener added to additionally resize the map should the window's size change.

The function itself returns an object with two references:

* .map contains a reference to the Raphael canvas itself and can be used to draw on top of the map or access the SVG node
* .states contains an object referencing all 52 paths, by postal abbreviation (or `US`), and can be used for applying additional Raphael .element methods such as styling or interactivity.