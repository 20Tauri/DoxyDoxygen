
:warning: If you have any problem to install/upgrade this plugin, please read the [Cannot Install topic](https://github.com/20Tauri/DoxyDoxygen/issues/103)


### Welcome to DoxyDoxygen

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/scr_first_word.gif)

DoxyDoxygen is a plug-in for [Sublime Text](https://www.sublimetext.com) that aims to save a lot of time and efforts when creating and updating documentation comments in source code.

How does it work ?

   * Write your code
   * Press <kbd>Alt</kbd>+<kbd>Q</kbd> (or `/**` + <kbd>Enter</kbd>), code is parsed and a skeleton documentation is written for you
   * Update your code
   * Press <kbd>Alt</kbd>+<kbd>Q</kbd>, documentation is updated

DoxyDoxygen can be easily configured to suit your needs.

   * no matter your programming language
   * no matter your documentation generator : [ApiDoc](http://apidocjs.com/), [AsDoc](http://help.adobe.com/en_US/flex/using/WSd0ded3821e0d52fe1e63e3d11c2f44bb7b-7fe7.html), [Doxygen](http://www.stack.nl/~dimitri/doxygen/), [Drupal Api Module](https://www.drupal.org/node/425940), [Google Closure](https://developers.google.com/closure/compiler/), [JavaDoc](http://docs.oracle.com/javase/7/docs/technotes/tools/windows/javadoc.html), [JsDoc](http://usejsdoc.org), [PhpDocumentor](https://www.phpdoc.org/docs/latest/index.html), [SassDoc](http://sassdoc.com/), [Sphinx](http://sphinx-doc.org/), [XmlDoc](http://www.ecma-international.org/publications/standards/Ecma-334.htm), [YuiDoc](http://yui.github.io/yuidoc)...
   * no matter your comment style : `/**`, `///`...
   * no matter your preferred layout for tags...

Documentation is generated... Descriptions are written in your native language...

And, reading this manual you will discover even more features like on demand translation...

### Usage

Create a documentation block
----------------------------

Start a documentation block (usually `/**`) before a declaration, then press <kbd>Enter</kbd>. The corresponding documentation will automatically be inserted. There are no keyboard shortcuts to memorize.

To be more efficient, you may also press <kbd>Alt</kbd>+<kbd>Q</kbd> (or <kbd>Super</kbd>+<kbd>Alt</kbd>+<kbd>Q</kbd> on OS X) after the function definition. A documentation block is written for you.

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/scr_python_calc_area_function.gif)

Types are automatically deduced from the code:

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/scr_javascript_guess_parameters_type.gif)

Even difficult to analyze programming languages are properly supported:

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/scr_cpp_calc_area_function.gif)

If a function has a template parameter, a `@tparam` property is automatically added:

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/scr_cpp_function_template.gif)

And, of course, classes (with template or not) are also supported.

Update / wrap an existing documentation block
---------------------------------------------

To update a comment, press <kbd>Alt</kbd>+<kbd>Q</kbd> (or <kbd>Super</kbd>+<kbd>Alt</kbd>+<kbd>Q</kbd> on OS X). As DoxyDoxygen knows the Doxygen commands, no invalid line break will be inserted.

Even better, with default settings, <kbd>Alt</kbd>+<kbd>Q</kbd> also reexamine the documented object and detects missing, renamed or moved parameters:

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/scr_cpp_update_existing_comment.gif)

DoxyDoxygen preserves list with hierarchy. On update, spaces before an item are kept. A valid list item is a line that start with `-#`, `-`, `+` or `*`.

Example of valid list

```javascript
/**
 * @return Error code
 *           - E_OK
 *           - E_ACCESS_DENIED
 *           - E_INTERNAL
 */
```
Example of invalid list

```javascript
/**
 * @return Error code:
 *           E_OK
 *           E_ACCESS_DENIED
 *           E_INTERNAL
 */
```

Invalid list after an update

```javascript
/**
 * @return Error code: E_OK E_ACCESS_DENIED E_INTERNAL
 */
```

Switch between comment styles
-----------------------------

To switch between your preferred comment styles, press <kbd>Shift</kbd>+<kbd>Alt</kbd>+<kbd>Q</kbd> (or <kbd>Super</kbd>+<kbd>Shift</kbd>+<kbd>Alt</kbd>+<kbd>Q</kbd> on OS X).

You can also find more flexible commands in the _Command Palette_.

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

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/scr_doxygen_syntax.gif)

### Comment continuation

As you can see on previous example, pressing <kbd>Enter</kbd> consecutively automatically continues the comment.

> **warning**
>
> On single line comment, comment continuation may appear as strange on the last line comment (`///`). The behavior is optional (see parameter `continuation_on_last_comment`). If activated, you can press <kbd>Shift</kbd>+<kbd>Enter</kbd> to stop continuation.

Navigate in documentation
-------------------------

### Move to the right column

To ease navigation, press End (<kbd>Super</kbd>+<kbd>Right</kbd> on OS X) on end-of-line to go to the next column.

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/scr_goto_eol.gif)

### Follow references

> **warning**
>
> Doxygen file only (`.dox`)

You can move from a `@ref` tag to the referenced page or section using the `goto_definition` command (press <kbd>F12</kbd> using Sublime Text default key bindings)

Fold / Unfold comments
----------------------

You can Fold / Unfold comments blocks from the _Command Palette_ or using Sublime Text standard shortcuts.

On Windows and Linux:

   * Ctrl+Shift+\[: Fold
   * Ctrl+Shift+\]: Unfold

On OS X:

   * Super+Alt+\[: Fold
   * Super+Alt+\]: Unfold

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/scr_fold_comment.gif)

Translate
---------

> **warning**
>
> Translations use network service. If you are behind a proxy, don't forget to configure it before using those features.

To translate selections, go to the _Command Palette_ (<kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>P</kbd>), then select _DoxyDoxygen: Translate_ or _DoxyDoxygen: Translate_ To to translate them.

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/scr_translate_to.gif)

> **tip**
>
> If a cursor is in a comment block (without selection), all descriptions of this comment will be translated.

Generate documentation
----------------------

If you use Doxygen, you can generate your documentation directly from the _Command Palette_. An assistant will help you to download tools and configure your project.

> **note**
>
> Before command execution, DoxyDoxygen parses the Doxyfile file and extract all heading `@INCLUDE`. For each included file, an environment variable s generated. The name of this variable is: `DOXYDOXYGEN_GENERATED_<base_name_without_extension>_PATH` and its value is the path where the file is stored. This allows relative inclusion inside each included file (useful for footer...)
>
> If the filename contains non alpha-numeric characters, they are replaced with `_`.
>
> -   `../path/filename.ext` defines a variable `DOXYDOXYGEN_GENERATED_FILENAME_PATH` with the value `../path`
> -   `path/A@STRANGE!VALUE.ext` defines a variable `DOXYDOXYGEN_GENERATED_A_STRANGE_VALUE_PATH` with the value `path`

> **tip**
>
> If you want to include it in your build chain, you can call this command from the command-line.


### User Guide

   * [Installation](http://20tauri.free.fr/DoxyDoxygen/v2/page_installation.php)
       * [Software installation with Package Control](http://20tauri.free.fr/DoxyDoxygen/v2/page_installation.php#software-installation-with-package-control)
       * [Manual software installation](http://20tauri.free.fr/DoxyDoxygen/v2/page_installation.php#manual-software-installation)
       * [License installation](http://20tauri.free.fr/DoxyDoxygen/v2/page_installation.php#license-installation)
       * [EULA (End User License Agreement)](http://20tauri.free.fr/DoxyDoxygen/v2/page_installation.php#eula-end-user-license-agreement)
   * [Usage](http://20tauri.free.fr/DoxyDoxygen/v2/page_usage.php)
       * [Create a documentation block](http://20tauri.free.fr/DoxyDoxygen/v2/page_usage.php#create-a-documentation-block)
       * [Update / wrap an existing documentation block](http://20tauri.free.fr/DoxyDoxygen/v2/page_usage.php#update-wrap-an-existing-documentation-block)
       * [Switch between comment styles](http://20tauri.free.fr/DoxyDoxygen/v2/page_usage.php#switch-between-comment-styles)
       * [Extend a documentation block](http://20tauri.free.fr/DoxyDoxygen/v2/page_usage.php#extend-a-documentation-block)
           * [Auto-completion](http://20tauri.free.fr/DoxyDoxygen/v2/page_usage.php#auto-completion)
           * [Comment continuation](http://20tauri.free.fr/DoxyDoxygen/v2/page_usage.php#comment-continuation)
       * [Navigate in documentation](http://20tauri.free.fr/DoxyDoxygen/v2/page_usage.php#navigate-in-documentation)
           * [Move to the right column](http://20tauri.free.fr/DoxyDoxygen/v2/page_usage.php#move-to-the-right-column)
           * [Follow references](http://20tauri.free.fr/DoxyDoxygen/v2/page_usage.php#follow-references)
       * [Fold / Unfold comments](http://20tauri.free.fr/DoxyDoxygen/v2/page_usage.php#fold-unfold-comments)
       * [Translate](http://20tauri.free.fr/DoxyDoxygen/v2/page_usage.php#translate)
       * [Generate documentation](http://20tauri.free.fr/DoxyDoxygen/v2/page_usage.php#generate-documentation)
   * [Customization](http://20tauri.free.fr/DoxyDoxygen/v2/page_customization.php)
       * [Settings](http://20tauri.free.fr/DoxyDoxygen/v2/page_customization.php#settings)
           * [Understanding settings](http://20tauri.free.fr/DoxyDoxygen/v2/page_customization.php#understanding-settings)
           * [Settings references](http://20tauri.free.fr/DoxyDoxygen/v2/page_customization.php#settings-references)
           * [Translation services settings](http://20tauri.free.fr/DoxyDoxygen/v2/page_customization.php#translation-services-settings)
       * [Add your own doc-style](http://20tauri.free.fr/DoxyDoxygen/v2/page_customization.php#add-your-own-doc-style)
       * [Key bindings](http://20tauri.free.fr/DoxyDoxygen/v2/page_customization.php#key-bindings)
           * [Key bindings on Windows and Linux](http://20tauri.free.fr/DoxyDoxygen/v2/page_customization.php#key-bindings-on-windows-and-linux)
           * [Key bindings on OS X](http://20tauri.free.fr/DoxyDoxygen/v2/page_customization.php#key-bindings-on-os-x)
       * [Commands from the palette](http://20tauri.free.fr/DoxyDoxygen/v2/page_customization.php#commands-from-the-palette)
       * [Commands from the menu](http://20tauri.free.fr/DoxyDoxygen/v2/page_customization.php#commands-from-the-menu)
   * [Glossary](http://20tauri.free.fr/DoxyDoxygen/v2/page_glossary.php)
   * [Appendices](http://20tauri.free.fr/DoxyDoxygen/v2/page_appendices.php)
       * [Features Comparison](http://20tauri.free.fr/DoxyDoxygen/v2/page_appendices.php#features-comparison)
       * [Supported Documentation Tools](http://20tauri.free.fr/DoxyDoxygen/v2/page_appendices.php#supported-documentation-tools)
       * [Supported Languages](http://20tauri.free.fr/DoxyDoxygen/v2/page_appendices.php#supported-languages)

### Support

   * [Known issues](http://20tauri.free.fr/DoxyDoxygen/v2/page_known_issues.php)
       * [Incorrect syntaxes](http://20tauri.free.fr/DoxyDoxygen/v2/page_known_issues.php#incorrect-syntaxes)
       * [Conflict with other plugins](http://20tauri.free.fr/DoxyDoxygen/v2/page_known_issues.php#conflict-with-other-plugins)
   * [FAQ](http://20tauri.free.fr/DoxyDoxygen/v2/page_faq.php)
       * [Can I call DoxyDoxygen from the command-line ?](http://20tauri.free.fr/DoxyDoxygen/v2/page_faq.php#can-i-call-doxydoxygen-from-the-command-line)
       * [Is it possible to disable default parameter description ?](http://20tauri.free.fr/DoxyDoxygen/v2/page_faq.php#is-it-possible-to-disable-default-parameter-description)
       * [How can I switch to a different `preferred_comment_style` ?](http://20tauri.free.fr/DoxyDoxygen/v2/page_faq.php#how-can-i-switch-to-a-different-preferred-comment-style)
       * [Is it possible to add tags dynamically ?](http://20tauri.free.fr/DoxyDoxygen/v2/page_faq.php#is-it-possible-to-add-tags-dynamically)
       * [Why there's no alignment on <kbd>Enter</kbd> ?](http://20tauri.free.fr/DoxyDoxygen/v2/page_faq.php#why-there-s-no-alignment-on-enter)
   * [Support](http://20tauri.free.fr/DoxyDoxygen/v2/page_support.php)
       * [Contact from GitHub](http://20tauri.free.fr/DoxyDoxygen/v2/page_support.php#contact-from-github)
       * [Contact from Web Site](http://20tauri.free.fr/DoxyDoxygen/v2/page_support.php#contact-from-web-site)
       * [Contact from Sublime Text](http://20tauri.free.fr/DoxyDoxygen/v2/page_support.php#contact-from-sublime-text)


### License

DoxyDoxygen may be downloaded and evaluated for free, however a license must be purchased for continued use.
See [End User License Agreement](http://20tauri.free.fr/DoxyDoxygen/v2/page_installation.php#eula-end-user-license-agreement) for further informations.

[![](https://www.paypalobjects.com/en_US/i/btn/btn_buynow_LG.gif)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=GXEEET3XT3VYG)

