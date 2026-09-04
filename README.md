## LaTeX Word Count <a href="https://packagecontrol.io/packages/LaTeX%20Word%20Count"><img src="https://packagecontrol.herokuapp.com/downloads/LaTeX%20Word%20Count.png"></a>

A [Sublime Text](https://www.sublimetext.com) word and character count plugin for LaTeX and plaintext files.

### Usage

LaTeX Word Count can be installed easily using [Sublime Text Package Control](https://packagecontrol.io/).

Go to `Tools -> Word Count` to display word, character and line counts for the current selection, or for the entire file if nothing is selected.

The default key binding is `Control + Shift + C`


## Installation

### By Package Control

1. Download & Install **`Sublime Text 3`** (https://www.sublimetext.com/3)
1. Go to the menu **`Tools -> Install Package Control`**, then,
    wait few seconds until the installation finishes up
1. Now,
    Go to the menu **`Preferences -> Package Control`**
1. Type **`Add Channel`** on the opened quick panel and press <kbd>Enter</kbd>
1. Then,
    input the following address and press <kbd>Enter</kbd>
    ```
    https://raw.githubusercontent.com/evandrocoan/StudioChannel/master/channel.json
    ```
1. Go to the menu **`Tools -> Command Palette...
    (Ctrl+Shift+P)`**
1. Type **`Preferences:
    Package Control Settings – User`** on the opened quick panel and press <kbd>Enter</kbd>
1. Then,
    find the following setting on your **`Package Control.sublime-settings`** file:
    ```js
    "channels":
    [
        "https://packagecontrol.io/channel_v3.json",
        "https://raw.githubusercontent.com/evandrocoan/StudioChannel/master/channel.json",
    ],
    ```
1. And,
    change it to the following, i.e.,
    put the **`https://raw.githubusercontent...`** line as first:
    ```js
    "channels":
    [
        "https://raw.githubusercontent.com/evandrocoan/StudioChannel/master/channel.json",
        "https://packagecontrol.io/channel_v3.json",
    ],
    ```
    * The **`https://raw.githubusercontent...`** line must to be added before the **`https://packagecontrol.io...`** one, otherwise,
      you will not install this forked version of the package,
      but the original available on the Package Control default channel **`https://packagecontrol.io...`**
    > [!WARNING]
    > Placing this custom channel before the default channel changes Package Control's resolution globally. Packages from this channel with the same name will override versions from the default channel.
    >
    > You can review the channel contents here:
    > https://raw.githubusercontent.com/evandrocoan/StudioChannel/master/channel.json
1. Now,
    go to the menu **`Preferences -> Package Control`**
1. Type **`Install Package`** on the opened quick panel and press <kbd>Enter</kbd>
1. Then,
    search for **`LaTeXWordCount`** and press <kbd>Enter</kbd>

See also:

1. [ITE - Integrated Toolset Environment](https://github.com/evandrocoan/ITE)
1. [Package control docs](https://packagecontrol.io/docs/usage) for details.


### LaTeX support

The main purpose of this plugin was to support reliable word counts for files with LaTeX markup. The plugin ignores the preamble, abstract, formulas, captions, and supports excluding headers, footnotes and appendices. Have a look at the available config options in `Preferences -> Package Settings -> LaTeX Word Count` to customise what gets counted.

### Suggestions

- Adding support for other ST-recognised markup languages should be pretty straightforward, have a look [here](https://github.com/kevinstadler/SublimeLaTeXWordCount/blob/master/WordCount.py#L64) to see how it's done for LaTeX and chip in!
- A real-time word count displayed in the status bar a la [WordCount](https://github.com/titoBouzout/WordCount) would be nice and not too hard to implement. If anyone's actually using this plugin and would like this feature just let me know and I'll add it!
- Sublime Text's `scope_name()` function could potentially be used to produce more robust stripping of LaTeX commands than the current regexp-wizardry.

### License

This plugin combines [a simple LaTeX word count python script](https://github.com/kevinstadler/bash-scripts/blob/master/wclatex) that I wrote in 2009, the basic plugin structure taken from Naomichi Yamakita's [string_counter](https://github.com/naomichi-y/string_counter), as well as changes and fixes submitted by [GitHub contributors](https://github.com/kevinstadler/SublimeLaTeXWordCount/graphs/contributors).

Released under the [MIT License](http://opensource.org/licenses/MIT)
