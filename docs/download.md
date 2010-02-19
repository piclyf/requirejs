# Download RequireJS

## Releases

### 0.8.0

#### require.js

All you need to start using require.js. Does not include i18n, text plugins or rhino support
Download: [Minified](release/0.8.0/minified/require.js) | [With Comments](release/0.8.0/comments/require.js)

#### require.js with plugins

require.js with the i18n and text plugins included.
Download: [Minified](release/0.8.0/minified/allplugins-require.js) | [With Comments](release/0.8.0/comments/allplugins-require.js)

### Optimization Tool / Full Source

A zip file that is the optimization tool for RequireJS. It also includes the full source for require.js and its plugins.

Use this download if you want to use RequireJS in Rhino.

[Download](release/0.8.0/requirejs-0.8.0.zip)

#### jQuery 1.4.1 with require()

A build of jQuery with integrated require() support. Just includes the basic RequireJS, does not have the following features:

* i18n, text plugins
* multiversion support
* page load support (it is assumed you will use jQuery's methods)
* require.modify() support

[Download: Minified](release/0.8.0/minified/require-jquery-1.4.2.js) | [With Comments](release/0.8.0/comments/require-jquery-1.4.2.js)

#### Sample jQuery 1.4.1 project with require()

A zip file containing a build of jQuery with integrated require() support, with an sample project included to show how it can be used when using jQuery. Does not include these features in RequireJS:

* i18n, text plugins
* multiversion support
* page load support (it is assumed you will use jQuery's methods)
* require.modify() support

[Download](release/0.8.0/jquery-require-sample.zip)

#### jQuery 1.4.1 with require() and plugins

A build of jQuery with integrated require() support and the i18n and text plugins. Does not include these other RequireJS features:

* multiversion support
* page load support (it is assumed you will use jQuery's methods)
* require.modify() support

Download: [Minified](release/0.8.0/minified/require.js) | [With Comments](release/0.8.0/comments/require.js)

#### Release Notes

* Renamed from RunJS to RequireJS
* Adds better support for existing JS files

<hr>
<hr>
<hr>

### Previous releases

The previous releases were just different stages in the source tree. Here are the release notes for those versions.

#### 0.0.7

* Separate module definitions via a require.def() function.
* Reworked module loading code based on Rawld Gill's algorithm.
* Changed i18n bundles to just list locales with true, based on a suggestion
  from Adam Peller.
* Integrating feedback from Bryan Forbes/David Mark.

#### 0.0.6

* Removed the Function specifier. That was for circular dependencies, but due to concerns about identity, decided to not support that use case. Now, a module function can return any value it wants to define itself, can be Function, Object, String, Number, Boolean, whatever. And now, for circular dependency, the circular dependency will be null. I decided not to throw in that case because I wan require to be able to load existing code that does not call back to require to define a module. To support circular dependencies, the module function can use require() to fetch that circular dependency later, outside the circular dependency loop.

#### 0.0.5

* Introduce plugin concept for require.js. i18n code moved to a plugin.

#### 0.0.4

* pause/resume for build layers

#### 0.0.3

* Module modifiers
* Better function module support
* Allow require() calls that just have a config object.

#### 0.0.2

* Allow modules to be defined with a plain object instead of a callback.
* i18n bundle support.

#### 0.0.1

* Basic module loading
* Support non-requirejs module loading, if file ends in .js
* Supports loading modules with different versions by using context names in
  top-level require() calls.