## DoxyDoxygen

Doxy.Doxygen is a SublimeText plug-in that allows you to auto-complete documentation block comments using Doxygen.

It was inspired by:
   - [DocBlockr](https://github.com/spadgos/sublime-jsdocs)
   - [DoxyDoc][https://github.com/Rapptz/DoxyDoc]

It's designed to provided a large support of languages (specialy c++ or non '/*' commented languages)

## Installation

The easy way to install this is through Package Control.

- Press Ctrl + Shift + P
- Type "install" without quotes to get to Package Control: Install Package
- Type "DoxyDoxygen" without quotes and you'll see this package.

Another way to install this is through running `git clone` of this repository in your package directory.

The command to do so is the following:

    git clone https://github.com/20Tauri/DoxyDoxygen.git DoxyDoxygen

## Usage

Insert comment introducer (ex: `/**` for C++, `##` for python), then <kbd>Enter</kbd> would automatically insert the corresponding documentation.
There are no keyboard shortcuts to memorise.

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/dox.gif)

As you can see, pressing <kbd>Enter</kbd> consecutively would automatically continue the comment.

When a definition is below the block, DoxyDoxygen detect it and prefill the documentation block.

For example, a function is trivial to document:

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/function.gif)

If a function has a template parameter, a `@tparam` property is automatically added:

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/template.gif)

Of course, class templated or not are also supported

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/templateclass.gif)

The wrap the comment, press <kbd>Alt</kbd>+<kbd>Q</kbd>.
DoxyDoxygen know the Doxygen commands and will NOT put unproper line break.

Better: <kbd>Alt</kbd>+<kbd>Q</kbd>, by default, reparse the documented object and may detect missing/renamed/deleted parameters field

![](https://raw.githubusercontent.com/20Tauri/DoxyDoxygen/master/images/reformat_advanced.gif)

To easy navigation, Press <bkd>EOL</bkd> on end-of-line, will go to the next column.

As you have probably already seen, DoxyDoxygen allows autocompletion of [Doxygen commands](http://www.stack.nl/~dimitri/doxygen/manual/commands.html). You can get a list of them by pressing <kbd>@</kbd> and a list will pop up automatically.
