## DoxyDoxygen

DoxyDoxygen is a SublimeText plug-in that allows you to auto-complete documentation block comments using Doxygen or JsDoc

It was inspired by:
   - [DocBlockr](https://github.com/spadgos/sublime-jsdocs)
   - [DoxyDoc](https://github.com/Rapptz/DoxyDoc)

It's designed to provided a large support of languages (specially c++ or non `/*` commented languages)


## Installation

The easy way to install this is through Package Control.
   - Press <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>P</kbd>
   - Type "install" without quotes to get to Package Control: Install Package
   - Type "DoxyDoxygen" without quotes and you'll see this package.

To install it manually:
   - Click the ```Preferences > Browse Packages... menu``` to open package directory
   - Download Package [DoxyDoxygen.sublime-package](http://20tauri.free.fr/DoxyDoxygen/lastest/DoxyDoxygen.sublime-package)
   - Copy it into the package directory
   - Restart Sublime Text

## Usage

### Create a documentation block

Insert a Doxygen comment introducer (ex: `##` for python) before a declaration, then <kbd>Enter</kbd> would automatically insert the corresponding documentation.

There are no keyboard shortcuts to memorize.

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/python.gif)

Types are automaticly deduce from code:

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/javascript.gif)

And hard to parse languages are well supported:

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/function.gif)

If a function has a template parameter, a `@tparam` property is automatically added:

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/template.gif)

Of course, class (with template or not) are also supported

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/templateclass.gif)

### Wrap and update an existing documentation

To wrap comment, press <kbd>Alt</kbd>+<kbd>Q</kbd>.
DoxyDoxygen know the Doxygen commands and will NOT put invalid line break.

Better: <kbd>Alt</kbd>+<kbd>Q</kbd>, by default, update the documented object and may detect missing/renamed/deleted parameters fields:

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/reformat_advanced.gif)

### Extend a documentation

DoxyDoxygen allows auto-completion of
    - [Doxygen commands](http://www.stack.nl/~dimitri/doxygen/manual/commands.html).
    - [JsDoc commands](http://usejsdoc.org/).

You can get a list of them by pressing <kbd>@</kbd> and a list will pop up automatically.

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/dox.gif)

As you can see, pressing <kbd>Enter</kbd> consecutively would automatically continue the comment.

### Navigate in documentation

To ease navigation, pressing <kbd>EOL</kbd> on end-of-line, will go to the next column.

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/eol.gif)

### Fold / Unfold comments

You can also Fold, Unfold all comments blocks, from the command palette or using Sublime Text standard shortcuts:
   -  <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>[</kbd>: Fold
   -  <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>]</kbd>: Unfold

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/fold.gif)

## Supported languages

Currently, following languages are supported:
   - C
   - C++
   - Python
   - Doxygen
   - Java
   - Javascript
   - Apex (using Java syntax)

And those languages cannot be parsed, but re-wrapped, continued...
   - ActionScript
   - Apex
   - Coffee
   - Groovy
   - Haxe
   - Lua
   - Objective C
   - Objective C++
   - Php
   - Rust
   - Scala
   - TypeScript
