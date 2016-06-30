Welcome to DoxyDoxygen
======================

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/first_word.gif)

DoxyDoxygen is a plug-in for [Sublime Text](https://www.sublimetext.com) that aims to save a lot of time and effort when creating and updating documentation comments in source code.

How does it work ?
   * Write your code
   * Press <kbd>Alt</kbd>+<kbd>Q</kbd> (or <kbd>Super</kbd>+<kbd>Alt</kbd>+<kbd>Q</kbd> on OS X), code is parsed and a skeleton documentation is written for you
   * Update your code
   * Press <kbd>Alt</kbd>+<kbd>Q</kbd>, documentation is updated

DoxyDoxygen can be easily configured to suit your needs.
   * no matter your programming language 
   * no matter your documentation generator : [ApiDoc](http://apidocjs.com/), [AsDoc](http://help.adobe.com/en_US/flex/using/WSd0ded3821e0d52fe1e63e3d11c2f44bb7b-7fe7.html), [Doxygen](http://www.stack.nl/~dimitri/doxygen/), [Drupal Api Module](https://www.drupal.org/node/425940), [Google Closure](https://developers.google.com/closure/compiler/), [JavaDoc](http://docs.oracle.com/javase/7/docs/technotes/tools/windows/javadoc.html), [JsDoc](http://usejsdoc.org), [PhpDocumentor](https://www.phpdoc.org/docs/latest/index.html), [SassDoc](http://sassdoc.com/), [Sphinx](http://sphinx-doc.org/), [XmlDoc](http://www.ecma-international.org/publications/standards/Ecma-334.htm), [YuiDoc](http://yui.github.io/yuidoc)...
   * no matter your comment style : `/**`, `///`...
   * no matter your preferred layout for tags...

Documentation is generated... Descriptions are written in your native language ...

Usage
=====

Create a documentation block
----------------------------

Start a documentation block (usually `/**`) before a declaration, then press <kbd>Enter</kbd>. The corresponding documentation will automatically be inserted. There are no keyboard shortcuts to memorize.

To be more efficient, you may also press <kbd>Alt</kbd>+<kbd>Q</kbd> (or <kbd>Super</kbd>+<kbd>Alt</kbd>+<kbd>Q</kbd> on OS X) after the function definition. A documentation block is written for you.

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/python.gif "Support Python")

Types are automatically deduced from the code:

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/javascript.gif "Guess types")

Even difficult to analyze programming languages are properly supported:

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/function.gif "Support C++")

If a function has a template parameter, a `@tparam` property is automatically added:

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/template.gif "Support @param")

And, of course, classes (with template or not) are also supported.

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/templateclass.gif "Document class")

Update / wrap an existing documentation block
---------------------------------------------

To update a comment, press <kbd>Alt</kbd>+<kbd>Q</kbd> (or <kbd>Super</kbd>+<kbd>Alt</kbd>+<kbd>Q</kbd> on OS X). As DoxyDoxygen knows the Doxygen commands, no invalid line break will be inserted.

Even better, with default settings, <kbd>Alt</kbd>+<kbd>Q</kbd> also reexamine the documented object and detects missing, renamed or moved parameters:

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/reformat_advanced.gif "Update existing comment")

DoxyDoxygen preserves list with hierarchy. On update, spaces before an item are kept. A valid list item is a line that start with `-#`, `-`, `+` or `*`.

```javascript
/**
 * @return Error code
 *           - E_OK
 *           - E_ACCESS_DENIED
 *           - E_INTERNAL
 */
```

```javascript
/**
 * @return Error code:
 *           E_OK
 *           E_ACCESS_DENIED
 *           E_INTERNAL
 */

/**
 * @return Error code: E_OK E_ACCESS_DENIED E_INTERNAL
 */
```

Switch between comment styles
-----------------------------

To switch between your preferred comment styles, press <kbd>Shift</kbd>+<kbd>Alt</kbd>+<kbd>Q</kbd> (or <kbd>Super</kbd>+<kbd>Shift</kbd>+<kbd>Alt</kbd>+<kbd>Q</kbd> on OS X).

You can also find more flexible commands in the Command Palette.

Extend a documentation block
----------------------------

### Auto-completion

DoxyDoxygen allows auto-completion. A large set of commands is available,

Available commands depends of doc-style:
   * [Commands list for ApiDoc](http://apidocjs.com/#params)
   * [Commands list for AsDoc](http://help.adobe.com/en_US/flex/using/WSd0ded3821e0d52fe1e63e3d11c2f44bc36-7ff6.html)
   * [Commands list for Doxygen](http://www.stack.nl/~dimitri/doxygen/manual/commands.html)
   * [Commands list for Drupal Api Module](https://www.drupal.org/coding-standards/docs)
   * [Commands list for Google Closure](https://developers.google.com/closure/compiler/docs/js-for-compiler?csw=1)
   * [Commands list for JavaDoc](http://docs.oracle.com/javase/7/docs/technotes/tools/windows/javadoc.html)
   * [Commands list for JsDoc](http://usejsdoc.org/)
   * [Commands list for PhpDocumentor](https://www.phpdoc.org/docs/latest/index.html)
   * [Commands list for SassDoc](http://sassdoc.com/annotations/)
   * [Commands list for Sphinx](http://sphinx-doc.org/markup/inline.html)
   * [Commands list for XmlDoc](http://www.stack.nl/~dimitri/doxygen/manual/xmlcmds.html)
   * [Commands list for YuiDoc](http://yui.github.io/yuidoc)

Only commands matching your configured doc-styles are suggested.

For example, to get the list of available commands, press `@`. Then, press <kbd>Ctrl</kbd>+<kbd>Space</kbd> to display the completion list.

<kbd>Ctrl</kbd>+<kbd>Space</kbd> is optional, but Sublime Text defaults settings deactivate completion in comment (see `auto_complete_selector` settings).

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/dox.gif "Support completion")

### Comment continuation

As you can see on previous example, pressing <kbd>Enter</kbd> consecutively automatically continues the comment.

> **warning**
>
> On single line comment, comment continuation may appear as strange on the last line comment (`///`). The behavior is optional (see parameter `continuation_on_last_comment`). If activated, you can press <kbd>Shift</kbd>+<kbd>Enter</kbd> to stop continuation.

Navigate in documentation
-------------------------

### Move to the right column

To ease navigation, press <kbd>End</kbd> (<kbd>Super</kbd>+<kbd>Right</kbd> on OS X) on end-of-line to go to the next column.

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/eol.gif "Intelligent move")

### Follow references

> **warning**
>
> Doxygen file only (`.dox`)

You can move from a `@ref` tag to the referenced page or section using the `goto_definition` command (press <kbd>F12</kbd> using Sublime Text default key bindings)

Fold / Unfold comments
----------------------

You can Fold / Unfold comments blocks from the Command Palette or using Sublime Text standard shortcuts.

On Windows and Linux:
   * Ctrl+Shift+\[: Fold
   * Ctrl+Shift+\]: Unfold

On OS X:
   * Super+Alt+\[: Fold
   * Super+Alt+\]: Unfold

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/fold.gif "Comment folding")

Translate
---------

> **warning**
>
> Translations use network service. If you are behind a proxy, don't forget to configure it before using those features.

To translate selections, go to the Command Palette (<kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>P</kbd>), then select DoxyDoxygen: Translate or DoxyDoxygen: Translate To to translate them.

![](http://20tauri.free.fr/DoxyDoxygen/v2/_images/scr_translate_to.gif)

> **tip**
>
> If a cursor is in a comment block (without selection), all descriptions of this comment will be translated.

Generate documentation
----------------------

If you use Doxygen, you can generate your documentation directly from the Command Palette. An assistant will help you to download tools and configure your project.

> **tip**
>
> If you want to include it in your build chain, you can call this command from the command-line .



Tips / FAQ / Customization...
-----------------------------

Please [visit the official web-site for further informations](http://20tauri.free.fr/DoxyDoxygen).


License
-------

DoxyDoxygen may be downloaded and evaluated for free, however a license must be purchased for continued use.
See [End User License Agreement](http://20tauri.free.fr/DoxyDoxygen/#page_eula) for further informations.

[![](https://www.paypalobjects.com/en_US/i/btn/btn_buynow_LG.gif)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=GXEEET3XT3VYG)

