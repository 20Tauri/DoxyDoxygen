## Welcome to DoxyDoxygen

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/demo.gif)

DoxyDoxygen is a SublimeText plugin that allows you to auto-complete documentation blocks using:

   * [Doxygen](http://www.stack.nl/~dimitri/doxygen/)
   * [Google Closure](https://developers.google.com/closure/compiler/)
   * [JavaDoc](http://docs.oracle.com/javase/7/docs/technotes/tools/windows/javadoc.html)
   * [JsDoc](http://usejsdoc.org)
   * [PhpDocumentor](http://www.phpdoc.org/docs/latest/index.html)
   * [XmlDoc](http://www.ecma-international.org/publications/standards/Ecma-334.htm)
   * [YuiDoc](http://yui.github.io/yuidoc)
   * ...

It's designed to provide:

   * a large support of languages (specially c++ or non `/*` commented languages),
   * a deep language comprehension (examine function body to determine parameters types),
   * an easy and powerfull documenting style configuration,
   * capacity to update existing comments,
   * sub-plugins support,
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

### Update / Wrap an existing documentation block

To wrap comment, press <kbd>Alt</kbd>+<kbd>Q</kbd> (or <kbd>Super</kbd>+<kbd>Alt</kbd>+<kbd>Q</kbd> on OS/X).
As DoxyDoxygen knows the Doxygen commands, no invalid lines break will be inserted.

Even better: with default settings, <kbd>Alt</kbd>+<kbd>Q</kbd> also updates the documented object and detect missing/renamed/moved parameters:

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/reformat_advanced.gif)

### Extend a documentation block

DoxyDoxygen allows auto-completion. A large set of commands is available, but only commands matching your selected DocStyles are suggested...

Available DocStyles and commands:

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

You can Fold / Unfold comments blocks from the command palette or using Sublime Text standard shortcuts.

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
   * Ruby (using Python syntax)
   * Rust (requiere to install the "rust" package)
   * Swift (requiere to install the "swift" package)
   * Apex (using Java syntax)
   * Groovy (using extended Java syntax)
   * ActionScript (generic parser)
   * AppleScript (generic parser)
   * Asp (generic parser)
   * Clojure (generic parser)
   * Lua (generic parser)
   * OCaml (generic parser)
   * Scala (generic parser)

And those languages cannot be parsed, but wrapped, continued...

   * Coffee
   * Dot
   * Erlang
   * Fortran
   * Haskell
   * Haxe
   * Lisp
   * MatLab
   * Objective C
   * Objective C++
   * Pascal
   * Perl
   * R
   * Shell Script (Bash)
   * SQL
   * TCL
   * TypeScript
   * VHDL
   * YAML
