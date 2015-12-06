## Welcome to DoxyDoxygen

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/demo.gif)

DoxyDoxygen is a SublimeText plugin that allows you to auto-complete documentation blocks using:

   * [ApiDoc](http://apidocjs.com/)
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

   * [ApiDoc](http://apidocjs.com/#params)
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

## Tips / FAQ

##### How can I switch to a different "preferred_comment_style" ?

On comment creation (<kbd>Enter</kbd>), DoxyDoxygen use the first preferered style that match the language. To use a specific comment style, you have to start your comment (ex: '///'), then press <kbd>Alt</kbd>+<kbd>Q</kbd>.

> _Note:_ For block style, you have to close it before pressing <kbd>Alt</kbd>+<kbd>Q</kbd> in it.


## Supported languages

Currently, following languages are supported:

   * ActionScript (generic parser)
   * Apex (using Java syntax)
   * AppleScript (generic parser)
   * Asp (generic parser)
   * C
   * C# 
   * C++
   * Clojure (generic parser)
   * Coffee (requiere to install the "coffescript" package)
   * Doxygen
   * Erlang (poor)
   * Haxe
   * Groovy (using extended Java syntax)
   * Java
   * JavaScript
   * Haskell (poor)
   * Lisp
   * Lua (generic parser)
   * MatLab
   * Objective C
   * Objective C++
   * OCaml (generic parser)
   * Pascal
   * Php
   * Python
   * R
   * Ruby
   * Rust (requiere to install the "rust" package)
   * Scala (generic parser)
   * SQL
   * Swift (requiere to install the "swift" package)
   * SystemVerilog (generic parser)
   * TCL
   * TypeScript

And those languages cannot be parsed, but wrapped, continued...

   * Assembler (x86, m68k, arm, sparc...)
   * Dot
   * Fortran
   * Perl
   * Shell Script (Bash)
   * VHDL
   * YAML

## Survey

To help to improve this software, I need to know your needs...
Here, you can find a short [survey](http://20tauri.free.fr/DoxyDoxygen/survey/index.php?survey=4cb7c9c).

## License

DoxyDoxygen may be downloaded and evaluated for free, however a license must be purchased for continued use. See
[End User License Agreement](http://20tauri.free.fr/DoxyDoxygen/#page_eula) for further informations.

[![](https://www.paypalobjects.com/en_US/i/btn/btn_buynow_LG.gif)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=GXEEET3XT3VYG)
