# My emacs settings

An ever-changing set of emacs settings. Micro-optimizations are super fun.
These are used in the [Emacs Rocks](http://emacsrocks.com) screencasts.

## Setup

To grab all the dependencies, either:

    git clone git://github.com/magnars/.emacs.d.git
    cd .emacs.d
    git submodule init
    git submodule update

or on git v1.6.5 or later:

    git clone --recursive git://github.com/magnars/.emacs.d.git


## Magit and clojure-mode

I don't keep magit in my .emacs.d. To install magit, do

    M-x package-list-packages

Search for `magit` and install it there.

The same is true for `clojure-mode` and `clojure-test-mode`. I haven't
been able to set it up properly for testing, but installing it through
the package system gets it right.

## Install emacs on mac

I use Cocoa Emacs, installed like this:

    brew install emacs --cocoa --use-git-head --HEAD

To open it with Alfred or Quicksilver, you have to copy `Emacs.app` into
`/Applications` instead of the symlink that brew places there.

## Tips for using these emacs settings

If you want to use my settings straight out of the box, here are some things to note:

 * The key bindings are optimized for a norwegian keyboard layout.

 * Start by reading up on all the cool stuff in key-bindings.el.

 * You quit emacs with `C-x r q`, mnemonic *Really Quit*.

 * Find file in project with `C-x o`, in dir with `C-x C-f`, recent with `C-x f`

 * Add your user- and project-specific stuff in .emacs.d/users/[machine name]/*.el

 * `C-h` is rebound to backspace, like in the shell. Get help on `F1` instead.

 * Autocomplete with `C-.`

 * expand-region is your friend. Find its bound key by doing `F1 f er/expand-region`

 * annoying-arrows suggests alternative ways of moving around if you use the
   arrow keys excessively.

 * Undo with `C-_` and redo with `M-_`. Watch the undo-tree with `C-x u`

 * Easily add functions to the F-keys with `M-: (f5 <sexps here>)`, example `(f5 (flush-lines "console.log"))`

 * Quickly jump anywhere in the buffer by pressing `fn` plus the starting letter of a word.

 * Indent and clean up white space in the entire buffer with `C-c n`

 * On a mac, the Meta key `M` is bound to Command.

 * I recommend rebinding Caps Lock to Ctrl and use that instead of the often badly placed Ctrl-key.

 * Watch [emacsrocks.com](http://emacsrocks.com)

## Survival guide for the first week of emacs

When you start using emacs for the first time, your habits fight you every inch
of the way. Your fingers long for the good old familiar keybindings. Here's an
overview of the most commonly used shortcuts to get you through this pain:

* `C      ` Shorthand for the ctrl-key
* `M      ` Shorthand for the meta-key (bound to cmd on my mac settings)
* `S      ` Shorthand for the shift-key

### Files

* `C-x C-f` Open a file. Starts in the current directory
* `C-x f  ` Open a recently visited file
* `C-x o  ` Open a file in the current project (based on .git ++)
* `C-x C-s` Save this file
* `C-x C-j` Jump to this files' current directory
* `C-x b  ` Switch to another open file (buffer)
* `C-x C-b` List all open files (buffers)

### Cut copy and paste

* `C-space` Start marking stuff. C-g to cancel.
* `C-w    ` Cut (aka kill)
* `C-k    ` Cut till end of line
* `M-w    ` Copy
* `C-y    ` Paste (aka yank)
* `M-y    ` Cycle last paste through previous kills
* `C-x C-y` Choose what to paste from previous kills
* `C-@    ` Mark stuff quickly. Press multiple times

### General

* `C-g    ` Quit out of whatever mess you've gotten yourself into
* `M-x    ` Run a command by name
* `C-.    ` Autocomplete
* `C-_    ` Undo
* `M-_    ` Redo
* `C-x u  ` Show the undo-tree
* `C-x m  ` Open magit. It's a magical git interface for emacs

### Navigation

* `C-arrow` Move past words/paragraphs
* `C-a    ` Go to start of line
* `C-e    ` Go to end of line
* `M-i    ` Go to indentation
* `M-g M-g` Go to line number
* `C-x C-i` Go to symbol
* `C-s    ` Search forward. Press `C-s` again to go further.
* `C-r    ` Search backward. Press `C-r` again to go further.

### Window management

* `C-x 0  ` Close this window
* `C-x 1  ` Close other windows
* `C-x 2  ` Split window horizontally
* `C-x 3  ` Split window vertically
* `S-arrow` Jump to window to the left/right/up/down

### Help

* `F1 t   ` Basic tutorial
* `F1 k   ` Help for a keybinding
* `F1 r   ` Emacs' extensive documentation
