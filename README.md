## DoxyDoxygen

DoxyDoxygen is a SublimeText plug-in that allows you to auto-complete documentation block comments using:
   - [Doxygen](http://www.stack.nl/~dimitri/doxygen/)
   - [JavaDoc](http://docs.oracle.com/javase/7/docs/technotes/tools/windows/javadoc.html)
   - [JsDoc](http://usejsdoc.org)
   - [YuiDoc](http://yui.github.io/yuidoc)
   - [PhpDocumentor](http://www.phpdoc.org/docs/latest/index.html)

It's designed to provide:
   - a large support of languages (specially c++ or non `/*` commented languages).
   - a deep language comprehension (examine function body to determine parameters types)
   - an easy and powerfull documenting style configuration
   - capacity to update existing comments
   - ...

## Usage

### Create a documentation block

Insert a Doxygen comment introducer (ex: `##` for python) before a declaration, then <kbd>Enter</kbd> would automatically insert the corresponding documentation.

There are no keyboard shortcuts to memorize.

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/python.gif)

Types are automaticly deduce from code:

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/javascript.gif)

Even hard to parse languages are well supported:

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/function.gif)

If a function has a template parameter, a `@tparam` property is automatically added:

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/template.gif)

And, of course, class (with template or not) are also supported

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/templateclass.gif)

### Wrap and update an existing documentation

To wrap comment, press <kbd>Alt</kbd>+<kbd>Q</kbd>.
And, as DoxyDoxygen know the Doxygen commands, NO invalid lines break will be inserted.

Even better: <kbd>Alt</kbd>+<kbd>Q</kbd>, by default, update the documented object and detect missing/renamed/deleted parameters fields:

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/reformat_advanced.gif)

### Extend a documentation

DoxyDoxygen allows auto-completion of
   - [Doxygen commands](http://www.stack.nl/~dimitri/doxygen/manual/commands.html).
   - [JavaDoc commands](http://docs.oracle.com/javase/7/docs/technotes/tools/windows/javadoc.html)
   - [JsDoc commands](http://usejsdoc.org/).
   - [YuiDoc commands](http://yui.github.io/yuidoc)
   - [PhpDocumentor commands](http://www.phpdoc.org/docs/latest/index.html)

You can get a list of them by pressing <kbd>@</kbd> and, according your sublime text settings, a list will pop up automatically.

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/dox.gif)

As you can see on previous example, pressing <kbd>Enter</kbd> consecutively would automatically continue the comment.

### Navigate in documentation

To ease navigation, pressing <kbd>EOL</kbd> on end-of-line, will go to the next column.

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/eol.gif)

### Fold / Unfold comments

You can also Fold / Unfold comments blocks, from the command palette or using Sublime Text standard shortcuts:
   - <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>[</kbd>: Fold
   - <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>]</kbd>: Unfold

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/fold.gif)

## Supported languages

Currently, following languages are supported:
   - C
   - C++
   - Doxygen
   - Java
   - JavaScript
   - Php
   - Python
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
   - Rust
   - Scala
   - TypeScript
