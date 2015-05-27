## DoxyDoxygen

DoxyDoxygen is a SublimeText plug-in that allows you to auto-complete documentation block comments using Doxygen.

It was inspired by:
   - [DocBlockr](https://github.com/spadgos/sublime-jsdocs)
   - [DoxyDoc](https://github.com/Rapptz/DoxyDoc)

It's designed to provided a large support of languages (specialy c++ or non '/*' commented languages)

## Installation

The easy way to install this is through Package Control.

- Press <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>P</kbd>
- Type "install" without quotes to get to Package Control: Install Package
- Type "DoxyDoxygen" without quotes and you'll see this package.

Another way to install this is through running `git clone` of this repository in your package directory.

The command to do so is the following:

    git clone https://github.com/20Tauri/DoxyDoxygen.git DoxyDoxygen

## Usage

### Create a documentation block

Insert a Doxygen comment introducer (ex: `##` for python) before a declaration, then <kbd>Enter</kbd> would automatically insert the corresponding documentation.

There are no keyboard shortcuts to memorize.

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/python.gif)

Another example, now using C++:

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/function.gif)

If a function has a template parameter, a `@tparam` property is automatically added:

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/template.gif)

Of course, class (with template or not) are also supported

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/templateclass.gif)

### Rewrap and reparse an existing documentation

The wrap the comment, press <kbd>Alt</kbd>+<kbd>Q</kbd>.
DoxyDoxygen know the Doxygen commands and will NOT put invalid line break.

Better: <kbd>Alt</kbd>+<kbd>Q</kbd>, by default, reparse the documented object and may detect missing/renamed/deleted parameters field

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/reformat_advanced.gif)

### Extend a documentation

DoxyDoxygen allows auto-completion of [Doxygen commands](http://www.stack.nl/~dimitri/doxygen/manual/commands.html). You can get a list of them by pressing <kbd>@</kbd> and a list will pop up automatically.

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/dox.gif)

As you can see, pressing <kbd>Enter</kbd> consecutively would automatically continue the comment.

### Navigate in documentation

To easy navigation, pressing <kbd>EOL</kbd> on end-of-line, will go to the next column.

