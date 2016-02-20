## Welcome to DoxyDoxygen

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/demo.gif)

DoxyDoxygen is a SublimeText plugin that allows you to auto-complete documentation blocks using:

   * [ApiDoc]
   * [AsDoc]
   * [Doxygen]
   * [Google Closure]
   * [JavaDoc]
   * [JsDoc]
   * [PhpDocumentor]
   * [SassDoc]
   * [Sphinx]
   * [XmlDoc]
   * [YuiDoc]
   * ...

It's designed to provide:

   * capability to *update* existing comments,
   * a [large support of languages](https://github.com/20Tauri/DoxyDoxygen/blob/master/COMPARE.md) (with more than 40 languages supported)
   * an easy and powerful documenting style configuration,
   * a deep language comprehension (examine function body to determine parameters types),
   * sub-plugins support,
   * ...

## Usage

### Create a documentation block

Insert a Doxygen comment introducer (ex: `##` for python) before a declaration, then <kbd>Enter</kbd> would automatically insert the corresponding documentation.

There are no keyboard shortcuts to memorize. But, to be more efficicent, you may also press <kbd>Alt</kbd>+<kbd>Q</kbd> after function definition.

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/python.gif "Support Python")

Types are automaticly deduce from code:

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/javascript.gif "Guess types")

Even hard to parse languages are well supported:

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/function.gif "Support C++"")

If a function has a template parameter, a `@tparam` property is automatically added:

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/template.gif "Support @param")

And, of course, class (with template or not) are also supported

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/templateclass.gif "Document class")

### Update / Wrap an existing documentation block

To wrap comment, press <kbd>Alt</kbd>+<kbd>Q</kbd> (or <kbd>Super</kbd>+<kbd>Alt</kbd>+<kbd>Q</kbd> on OS/X).
As DoxyDoxygen knows the Doxygen commands, no invalid lines break will be inserted.

Even better: with default settings, <kbd>Alt</kbd>+<kbd>Q</kbd> also updates the documented object and detect missing/renamed/moved parameters:

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/reformat_advanced.gif "Update existing comment")

### Switch between commenting styles

To switch between your preferred commenting styles, press <kbd>Alt</kbd>+<kbd>Shift</kbd>+<kbd>Q</kbd> (or <kbd>Super</kbd>+<kbd>Alt</kbd>+<kbd>Shift</kbd>+<kbd>Q</kbd> on OS/X).

You can also find more flexible commands in the palette.

### Generate documentation

If you use Doxygen, you can generate your documentation directly from the palette.
An assistant will help you to download tools and configure your project.

### Extend a documentation block

DoxyDoxygen allows auto-completion. A large set of commands is available, but only commands matching your selected DocStyles are suggested...

Available DocStyles and commands:

   * [ApiDoc](http://apidocjs.com/#params)
   * [AsDoc](http://help.adobe.com/en_US/flex/using/WSd0ded3821e0d52fe1e63e3d11c2f44bc36-7ff6.html)
   * [Doxygen](http://www.stack.nl/~dimitri/doxygen/manual/commands.html).
   * [Google Closure Compiler](https://developers.google.com/closure/compiler/docs/js-for-compiler?csw=1)
   * [JavaDoc](http://docs.oracle.com/javase/7/docs/technotes/tools/windows/javadoc.html)
   * [JsDoc](http://usejsdoc.org/).
   * [PhpDocumentor](http://www.phpdoc.org/docs/latest/index.html)
   * [Sphinx](http://sphinx-doc.org/markup/inline.html)
   * [XmlDoc](http://www.stack.nl/~dimitri/doxygen/manual/xmlcmds.html)
   * [YuiDoc](http://yui.github.io/yuidoc)

You can get a list of them by pressing <kbd>@</kbd> and, according your sublime text settings, a list will pop up automatically.

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/dox.gif "Support completion")

As you can see on previous example, pressing <kbd>Enter</kbd> consecutively would automatically continue the comment.

### Navigate in documentation

To ease navigation, pressing <kbd>EOL</kbd> (<kbd>Super</kbd>+<kbd>Right</kbd> on OS/X) on end-of-line, will go to the next column.

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/eol.gif "Intelligent move")

### Fold / Unfold comments

You can Fold / Unfold comments blocks from the command palette or using Sublime Text standard shortcuts.

On Windows and Linux:

   * <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>[</kbd>: Fold
   * <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>]</kbd>: Unfold

On OS/X:

   * <kbd>Super</kbd>+<kbd>Alt</kbd>+<kbd>[</kbd>: Fold
   * <kbd>Super</kbd>+<kbd>Alt</kbd>+<kbd>]</kbd>: Unfold

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/fold.gif "Comment folding")

## Tips / FAQ

##### How can I switch to a different "preferred_comment_style" ?

On comment creation (<kbd>Enter</kbd>), DoxyDoxygen use the first preferered style that match the language. To use a specific comment style, you have to start your comment style (ex: '// ='), then press <kbd>Alt</kbd>+<kbd>Q</kbd>.

> _Note:_ For block style, you have to close it before pressing <kbd>Alt</kbd>+<kbd>Q</kbd> in it.

##### How to avoid comment continuation ?

Comment continuation is optionnal (parameter `continuation_on_last_comment`), but if activated, you can press <kbd>Shift</kbd>+<kbd>Return</kbd> to stop continuation.

> _Note:_ For block style, you have to close it before pressing <kbd>Alt</kbd>+<kbd>Q</kbd> in it.

##### How can I add tags dynamicly ?

Since version 0.27, `block_layout` parameter may be context dependant. To set up a context dependant, you have to define a list of dictionnaries.

Each dictionnary should have two keys:

   * `block_layout` (same format a if it's an array of string)
   * `context` similar format as sublime text rule

Each context, is a list of conditions. Each condition is composed by

   * `key`: Name of a context operand to query. May be one of:
      * `kind`
         * "function", "lambda", "generator", "constructor",
         * "class", "struct", "union", "enum"
         * "var", "constant"
      * `name`
      * `nb_params` (only for "function", "lambda"...)
      * `nb_tparams`
      * `row`
      * `col`
   * `operator`: Type of test to perform against `key`. May be one of:
      * `regex_match`
      * `equal`
      * `not_equal`
      * `greater_than`
      * `lower_than`
      * `regex_contains`
   * `operand`: Value against which the result of `key` is tested.

Here's an example illustrating most of the features outlined above:
```
    "block_layout": {
        "Doxygen": [
           {
               "tags": [
                   "@brief            I'm the {name} class"
               ],
               "context": [
                   { "key": "name",      "operator": "regex_match",    "operand": "^_.*$" },
                   { "key": "kind",      "operator": "equal",          "operand": "class" }
               ]
           },

           // Autofill description for getters
           {
               "tags": [
                   "@brief            Get {name:doxy_words(1,);doxy_lower();}",
                   "@return           {name:doxy_words(1,);doxy_capitalize();}"
               ],
               "context": [
                   { "key": "name",      "operator": "regex_match",          "operand": "get[A-Z_].*" },
               ]
           },

           // File Header integration
           {
               "tags": [
                   "@brief            I'm a file header and my name is {file_base_name}",
                   "",
                   "@author           {user_name}",
                   "",
                   "@date             {now:%d-%b-%Y}"
               ],
               "context": [
                   { "key": "row",      "operator": "equal",          "operand": "0" },
                   { "key": "kind",     "operator": "equal",          "operand": "" }
               ]
           },

           // Compact style if there's less than one parameter
           {
               "tags": [
                   "@brief",
                   "@param",
                   "@tparam",
                   "@return",
                   ""
               ],
               "context": [
                   { "key": "nb_params", "operator": "lower_than",     "operand": "2" }
               ]
           }

           // You don't have to be exhautive.
           // If no rule match, 'block_layout_default' is considered
       ]
   }
```

[ApiDoc]: http://apidocjs.com/
[AsDoc]: http://help.adobe.com/en_US/flex/using/WSd0ded3821e0d52fe1e63e3d11c2f44bb7b-7fe7.html
[DoxyDoxygen]: https://github.com/20Tauri/DoxyDoxygen
[Doxygen]: http://www.stack.nl/~dimitri/doxygen/
[Google Closure]: https://developers.google.com/closure/compiler/
[JavaDoc]: http://docs.oracle.com/javase/7/docs/technotes/tools/windows/javadoc.html
[JsDoc]: http://usejsdoc.org
[PhpDocumentor]: http://www.phpdoc.org/docs/latest/index.html
[SassDoc]: http://sassdoc.com/
[Sphinx]: http://sphinx-doc.org/
[XmlDoc]: http://www.ecma-international.org/publications/standards/Ecma-334.htm
[YuiDoc]: http://yui.github.io/yuidoc

## Survey

To help to improve this software, I need to know your needs... Here, you can find some surveys:

   * [survey #1](http://20tauri.free.fr/DoxyDoxygen/survey/index.php?survey=4cb7c9c).
   * [survey #2](http://20tauri.free.fr/DoxyDoxygen/survey/index.php?survey=762ed51).

## License

DoxyDoxygen may be downloaded and evaluated for free, however a license must be purchased for continued use. See
[End User License Agreement](http://20tauri.free.fr/DoxyDoxygen/#page_eula) for further informations.

[![](https://www.paypalobjects.com/en_US/i/btn/btn_buynow_LG.gif)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=GXEEET3XT3VYG)

**SPECIAL OFFER (until 31st march 2016) - 33% discount**

Buy 2 licenses a third one will be offered. Current price is 6 euros per license.
With this offer (that reduce PayPal fee), price is only 4 euros per license.

To be fair, if your are previously licensed user and one of your friend/colleague buy a
license during this period, a third one will be offer. The new buyer simply have to send
an email to "you, me, person that will receive the license". The individual license will
be sent directly to this person after a week.
