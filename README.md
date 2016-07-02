# dwmframe
Basic CSS framework used for [edG Design](http://edgdesign.co) and my personal projects. 

## Overview
Uses Sass, [SCSS](http://sass-lang.com/documentation/file.SASS_REFERENCE.html) syntax. 

Everything is imported via the dwmframe.scss manifest file. Style partials in /core are required, those in /modules are optional. 

Latest version compatible with old projects: 1.1.0

## Usage
Install with Bower. Not currently registered with Bower, so: 
~~~~
bower install git@github.com:davidwmartin/dwmframe.git
~~~~

## TODO 

### Misc
1. Annotate
2. Strategy for importing directly from local project's scss manifest, to allow overrides of specific framework files.
3. Rename defaults partial?

### Modular Scale
1. Function for calculating scale degrees

### Grid
1. Grid mixins
2. Mobile first?

### Typography
1. Better defaults for mobile typography (mainly size) 
2. "relative" modular scale if possible -- so that I can, for example, set an element to be one scale degree larger / smaller than it's parent
