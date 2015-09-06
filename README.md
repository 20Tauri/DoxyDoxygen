## DoxyDoxygen

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/demo.gif)

DoxyDoxygen is a SublimeText plug-in that allows you to auto-complete documentation block comments using:

   * [Doxygen](http://www.stack.nl/~dimitri/doxygen/)
   * [Google Closure](https://developers.google.com/closure/compiler/)
   * [JavaDoc](http://docs.oracle.com/javase/7/docs/technotes/tools/windows/javadoc.html)
   * [JsDoc](http://usejsdoc.org)
   * [PhpDocumentor](http://www.phpdoc.org/docs/latest/index.html)
   * [XmlDoc](http://www.ecma-international.org/publications/standards/Ecma-334.htm)
   * [YuiDoc](http://yui.github.io/yuidoc)

It's designed to provide:

   * a large support of languages (specially c++ or non `/*` commented languages),
   * a deep language comprehension (examine function body to determine parameters types),
   * an easy and powerfull documenting style configuration,
   * capacity to update existing comments,
   * plugins supports,
   * ...

## Usage

### Create a documentation block

Insert a Doxygen comment introducer (ex: `##` for python) before a declaration, then <kbd>Enter</kbd> would automatically insert the corresponding documentation.

There are no keyboard shortcuts to memorize. But, to be more efficicent, you may also press <kbd>Alt</kbd>+<kbd>Q</kbd> after function definition.

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

To wrap comment, press <kbd>Alt</kbd>+<kbd>Q</kbd> (or <kbd>Super</kbd>+<kbd>Alt</kbd>+<kbd>Q</kbd> on OS/X).
And, as DoxyDoxygen know the Doxygen commands, NO invalid lines break will be inserted.

Even better: <kbd>Alt</kbd>+<kbd>Q</kbd>, by default, update the documented object and detect missing/renamed/deleted parameters fields:

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/reformat_advanced.gif)

### Extend a documentation

DoxyDoxygen allows auto-completion. Available commands:

   * [Doxygen](http://www.stack.nl/~dimitri/doxygen/manual/commands.html).
   * [Google Closure Compiler](https://developers.google.com/closure/compiler/docs/js-for-compiler?csw=1)
   * [JavaDoc](http://docs.oracle.com/javase/7/docs/technotes/tools/windows/javadoc.html)
   * [JsDoc](http://usejsdoc.org/).
   * [PhpDocumentor](http://www.phpdoc.org/docs/latest/index.html)
   * [XmlDoc](http://www.stack.nl/~dimitri/doxygen/manual/xmlcmds.html)
   * [YuiDoc](http://yui.github.io/yuidoc)

You can get a list of them by pressing <kbd>@</kbd> and, according your sublime text settings, a list will pop up automatically.

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/dox.gif)

As you can see on previous example, pressing <kbd>Enter</kbd> consecutively would automatically continue the comment.

### Navigate in documentation

To ease navigation, pressing <kbd>EOL</kbd> (<kbd>Super</kbd>+<kbd>Right</kbd> on OS/X) on end-of-line, will go to the next column.

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/eol.gif)

### Fold / Unfold comments

You can also Fold / Unfold comments blocks, from the command palette or using Sublime Text standard shortcuts.

On Windows and Linux:

   * <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>[</kbd>: Fold
   * <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>]</kbd>: Unfold

On OS/X:

   * <kbd>Super</kbd>+<kbd>Alt</kbd>+<kbd>[</kbd>: Fold
   * <kbd>Super</kbd>+<kbd>Alt</kbd>+<kbd>]</kbd>: Unfold

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/fold.gif)

## Supported languages

Currently, following languages are supported:

   * C
   * C++
   * C# 
   * Doxygen
   * Java
   * JavaScript
   * Php
   * Python
   * Rust (<kbd>Alt</kbd>+<kbd>Q</kbd> requiere to install the "rust" package)
   * Swift (<kbd>Alt</kbd>+<kbd>Q</kbd> requiere to install the "swift" package)
   * Apex (using Java syntax)
   * Groovy (using Java syntax)

And those languages cannot be parsed, but re-wrapped, continued...

   * ActionScript
   * Coffee
   * Fortran
   * Haskell
   * Haxe
   * Lua
   * MatLab
   * Objective C
   * Objective C++
   * OCaml
   * Pascal
   * Ruby
   * Scala
   * Tcl
   * TypeScript
   * Vhdl
