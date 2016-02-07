## Useful packages ##

*You can download a `.zip` containing all of the packages mentioned below [here](../assets/my-sublime-setup/packages.zip).*

<video src='../assets/my-sublime-setup/alignment.mov' style='width: 200px; margin: 20px; float: right' autobuffer='autobuffer' autoplay loop></video>

#### Alignment ####

The easiest way to single-handedly make a block of code more readable is to align its contents, whether it's the values of a hash or the equals signs initializing a handful of variables at the beginning of a method. However, it's a pain the butt (and frankly not worth the time) to manually go through line-by-line adding the right spacing. With the Sublime alignment package, you can simply select the parts of the lines you want to be aligned and hold down `cmd + ctrl + a` to achieve the same result. (In the short recorded example to the right, I held down the `opt` button while dragging my mouse along the beginning of each line to select the relevant lines even faster.)

Thanks to [John Backus](https://twitter.com/backus) for sharing this package with me.

#### All Autocomplete ####

Extends Sublime's autocompletion to find matches in all open files.

#### AutoSpell ####

Auto-replaces obvious spelling mistakes in `.md` and `.txt` files.

#### Bracket Highlighter ####

Highlights or underlines the innermost brackets of the code you're currently editing. You can see it in action in the alignment video above.


#### FileDiffs ####

Enables you to run quick diffs between any combination of open tabs, your clipboard, and files from the current project.

#### Fold Comments ####

Quickly fold all comments in the current document.

<img src='../assets/my-sublime-setup/gitgutter-ex.png' style='float: right; width: 340px; margin: 20px'/>

#### GitGutter ####

Small, unobtrusive symbols to the left gutter of Sublime indicate the lines' git status (if you are in a git repository).

#### Origami ####

Allows you to split Sublime into panes however you like with simple keyboard shortcuts. You can find my custom key bindings below, which include extensions to Origami's default shortcuts.

#### Package Resource Viewer ####

Enables quick viewing and editing of all your packages. It's a bit shocking that this doesn't come with Sublime by default; without this, you have to manually go through the bowels of your file system to find any `.tmLanguage`, `.sublime-package`, etc. files that you wanted to edit. In contrast, this plugin gives you fuzzy search over all of these packages directly from Sublime. In short –– it's great!

#### Ruby Markers ####

Executes Ruby code and updates `# =>` markers with the results. This one is particularly useful for demoing features of the language or testing the output of little scripts as you write them. If you've ever seen [Ruby Tapas](http://www.rubytapas.com/) (and if you haven't, you should!!!!), Avdi uses `xmpfilter` and `rcodetools` with Emacs to get this same behavior for his mini tutorials.

<img src='../assets/my-sublime-setup/ruby-markers.gif' style='margin: 10px; width: 95%'/>

Note that you may have to change the package settings from `"ruby_manager": "auto"` to `"ruby_manager": "rvm"` in order to get this to work.

Thanks to [John Backus](https://twitter.com/backus) for sharing this package with me.

#### Schemr & Themr ####

These two packages enable you to quickly cycle through color schemes and themes (respectively) from any file rather than having to open your preferences file, manually update their file paths, switch back to your original open file to see the changes, and repeat each time you want to test out a new style. These packages aren't so critical for long-term use (I haven't changed my theme in months, and I don't plan on doing so in the near future), but they are really nice when you are first setting up your coding environment.

