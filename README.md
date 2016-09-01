# dwmframe

## Overview
Basic CSS framework used for my company  - [edG Design](http://edgdesign.co) - and personal projects. 

Uses Sass, [SCSS](http://sass-lang.com/documentation/file.SASS_REFERENCE.html) syntax. 

Everything is imported via the dwmframe.scss manifest file. Style partials in /core are required, those in /modules are optional. Framework variable defaults are given in _variables.scss 

*Note to self: Last version compatible with old projects is 1.1.0*

## Usage

### Installation
Install with Bower. Not currently registered with Bower, so: 
~~~~
bower install git@github.com:davidwmartin/dwmframe.git
~~~~

### Grid
Mobile-first, inline-block based grid. There are three grid sizes, built around two breakpoints. Grid classes can be found in /core/_grid.scss, breakpoint variables & defaults in _variables.scss. Breakpoint variables define the upper-limit of a grid prefix.

1. Small-sized / Mobile grid is prefixed with "palm"
	* Grid class: palm-1-2
	* Breakpoint: $palm-end
	* Available proportions: 1/4,1/3,1/2
2. Mid-sized / Tablet grid is prefixed with "tab"
	* Grid class: tab-1-2
	* Breakpoint: $tab-end
	* Available proportions: 1/8, 1/6, 1/4, 1/3, 1/2
3. Large-sized / Desktop grid is prefixed with "desk"
	* Grid class: desk-1-2
	* Available proportions: 1/8, 1/6, 1/5, 1/4, 1/3, 1/2

#### Grid Usage
* **Grid wrapper:** 
	* Defined by class: .gw -- max width is defined by $content-max variable. Wrapper element is centered in the view. 
* **Grid elements:** 
	* must have the .g class and sizing classes. 
	* Sizing classes are the prefix for the grid size ("palm", "tab", "desk") followed by a fraction representing the proportional width of the element. So for an element that takes up 1/2 of it's container on mobile, use ".palm-1-2"; for an element to fill 100% (1/1) of it's container on full sized screens, use ".desk-1-1"
	* *Note on fractions: reduce your fractions -- there are no predefined classes for 2/6ths, but there are for 1/3rd.*
* In general, avoid applying styles to either the .gw or .g classes. The exception is applying a "vertical-align" rule to specific elements with the .g class. 
* Grid is mobile first -- so an element will retain it's mobile-grid width unless that is overridden at larger sizes (e.g. an element with "palm-1-2" will be 50% width at all sizes unless a "tab-" or "desk-" class with different proportion is applied to it).

### Modular Scale

Two-stranded modular scale. Base values are $base-1 and $base-2 -- respective ratios are $ratio-1 and $ratio-2. Modular scale values are calculated for 5 degrees above the base, and 2 below. $mds-1 is scale one, base degree (so equal to $base-1) -- this is the size used for all text by default. One degree up the first modular scale is $mds-1-1 (for one degree up the second scale, use $mds-2-1). One degree down the first modular scale is $mds-1-a (for the second scale it's $mds-2-a). 

For more information on modular scales, and a handy calculator, go to [modularscale.com](http://www.modularscale.com/)

## TODO 

### Misc
- Strategy for importing directly from local project's scss manifest, to allow overrides of specific framework files.
- Flesh out button styles
- Remove button variables?
- Add Normalize as bower dependency
- Update link visited / hover color strategy, variables
- "text-decoration:none" on buttons
- add normalize-scss as a dependency

### Modular Scale
- Function for calculating scale degrees
- "relative" modular scale if possible -- so that I can, for example, set an element to be one scale degree larger / smaller than it's parent

### Grid
- Grid mixins
- Desktop first version?
- Padding variables
- Auto-calculated grid widths, so I could make new proportions on the fly, just by using the class
- add 1/5 to tablet size? mobile?
- ADD NOTE TO INSTRUCTIONS ABOUT WHITESPACE / MARGIN LEFT ISSUE FOR INLINE BLOCK ELEMENTS
- name breakpoint variables by start instead of end? (tab-start, desk-start)

### Forms
- .form-element container styles? 


### Typography
1. Better defaults for mobile typography (mainly size)
-- LOOK INTO WHERE I REMOVED LINE HEIGHT AND FONT SIZE FROM COPY ELEMENTS...

### Buttons
- variables for color, padding, etc for each of the 3 button sizes & types?