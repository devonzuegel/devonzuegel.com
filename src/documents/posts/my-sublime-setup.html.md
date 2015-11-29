---
title: My text editor is absolutely sublime
author: Devon Zuegel
tags: ['sublime text', 'theme', 'text editing', 'programming', 'workflow optimization' ]
collection: posts
date_published: 2015-11-28
img: https://d13yacurqjgara.cloudfront.net/users/13536/screenshots/1022371/sublime-text_teaser.png
workflow: true
---

I am a huge fan of Sublime Text. It is beautiful and easy to use fresh out of the box, and it does everything I need it to do. However, my favorite characteristic of Sublime is that it is *extremely* extensible. I have (perhaps too obsessively) customized my editor so much to the point that many people don't recognize it as Sublime, and because I've been able to mold it behavior to fit my needs. I find that I'm much more productive on it than with any other editor, including others' versions of Sublime.

I love sharing little tips and tricks I've incorporated into my workflow, so I'm excited to write up this post surveying the key customizations I've made. I hope you enjoy reading it as much as I've enjoyed writing it.

Better yet, I love learning new ways to better use Sublime! If there's anything here that I've missed, feel free to [email](mailto:devonz@cs.stanford.edu) or [tweet](http://twitter.com/devonzuegel) at me with your additions.

## Useful Key Bindings ##

| **Shortcut**                 | **Result**                                            |
| --                           | --                                                    |
| select, `cmd + g`            | Selects all instances of the originally selected text |
| select, `cmd + d`            | Similar to `cmd + g`, except it adds each following instance one at a time                                                                 |
| `cmd + f`                    | search current document for string (or regex, if the `*` button to the left is toggled on)                                                      |
| `cmd + shift + f`            | expanded find menu; find & replace; advanced search, enabling you to specify what folders / types of files you wish to search               |
| `cmd + shift + i` | Auto indents code (works better for languages like C++ or Ruby, which have block endings defined more than just whitespace)                            |
| `ctrl + cmd + up/down arrow` | Move current line(s) up/down                          |
| `cmd + shift + d`            | Duplicate current line(s)                             |
| `cmd + x`                    | Cut current line(s)                                   |
| hold `cmd` while selecting   | Make multiple selections                              |
| `opt + drag cursor`          | Make multiple selections (alternate)                  |
| `cmd + k + 1`                | Fold 1st layer of code (replace `1` with `2, 3, ...` to fold 2nd, 3rd, ... layers)                                                             |

## My theme & color scheme ##

A Sublime color scheme defines the syntax highlighting and canvas color of your editor, while a theme defines the styling of the sidebars, tabs, and find-and-replace menu.

#### Pisco Sour color scheme ####

- You can download my Pisco Sour color scheme [here]((../assets/my-sublime-setup/pisco-sour.tmTheme).
- I created this theme with [tmTheme Editor](http://tmtheme-editor.herokuapp.com). Feel free to use or update my theme however you want.

#### Spaceblack theme ####

- You can download the Spaceblack theme [here]((../assets/my-sublime-setup/Spaceblack.sublime-theme).

#### Screenshots ####

Here are a few screenshots of my Sublime setup:

| **Multimarkdown** | **Python**  |
| :---:             | :---:       |
| ![](../assets/my-sublime-setup/md-sample.png) | ![](../assets/my-sublime-setup/py-sample.png) |
| **Ruby**          | **Haskell** |
| ![](../assets/my-sublime-setup/rb-sample.png) | ![](../assets/my-sublime-setup/hs-sample.png) |

## My User Preferences files ##

Sublime User Preferences files are where you define your color scheme, theme, and a variety of other customizations like line padding, minimap toggling, and line highlighting. You can find your `/User/Preferences.sublime-settings` file by pressing `cmd + /` or by going up to the **Sublime Text > Preferences > Settings – User** menu. Here is my User Preferences file:

<script src="https://gist.github.com/devonzuegel/814f072e819d83873932.js"></script>

Sublime allows allows you to define language-specific user preferences. This particularly comes in handy for Markdown and plain-text editing, since they are so different from programming-centric uses of Sublime. For instance, I prefer not to have lines wrap around while I'm programming, but I can't live without it while working with real paragraphs rather than concise lines of code that are < 80 characters long. Also, I prefer my code-left-aligned, while I like having broad margins on either side of my text while writing.

To access and edit language-specific preference files, go to **Sublime Text > Preferences > Package Settings > Markdown Editing > MultiMarkdown Settings –– User** (replacing "Markdown Editing" and "Multimarkdown Settings –– User" with the language with which you're working).

<script src="https://gist.github.com/devonzuegel/a5d84bef5bdfc03008b9.js"></script>

## Useful packages ##

You can download a `.zip` of the packages mentioned below [here](../assets/my-sublime-setup/packages.zip)

<video src='../assets/my-sublime-setup/alignment.mov' style='width: 200px; margin: 20px; float: right' autobuffer='autobuffer' autoplay></video>

#### Alignment ####

The easiest way to single-handedly make a block of code more readable is to align its contents, whether it's the values of a hash or the equals signs initializing a handful of variables at the beginning of a method. However, it's a pain the butt (and frankly not worth the time) to manually go through line-by-line adding the right spacing. With the Sublime alignment package, you can simply select the parts of the lines you want to be aligned and hold down `cmd + ctrl + a` to achieve the same result. (In the short recorded example to the right, I held down the `opt` button while dragging my mouse along the beginning of each line to select the relevant lines even faster.)

#### All Autocomplete ####

Extends Sublime's autocompletion to find matches in all open files.

#### AutoSpell ####

Auto-replace obvious spelling mistakes in `.md` and `.txt` files.

#### Bracket Highlighter ####

Highlights or underlines the innermost brackets of the code you're currently editing. You can see it in action in the alignment video above.

#### Emmett ####

Allows you to expand css-like abbreviations to markup. For example, when you press `TAB` it dynamically parses this...:

```sass
ul#nav>li.items$*4>a{Item $}
```

... to the following:

```html
<ul id="nav">
    <li class="items1"><a href="">Item 1</a></li>
    <li class="items2"><a href="">Item 2</a></li>
    <li class="items3"><a href="">Item 3</a></li>
    <li class="items4"><a href="">Item 4</a></li>
</ul>
```

#### FileDiffs ####

Enables you to run quick diffs between any combination of open tabs, your clipboard, and files from the current project.

#### Fold Comments ####

Quickly fold all comments in the current document.

<img src='../assets/my-sublime-setup/gitgutter-ex.png' style='float: right; width: 340px; margin: 20px'/>

#### GitGutter ####

Small, unobtrusive symbols to the left gutter of Sublime indicate the lines' git status (if you are in a git repository).

#### Origami ####

Allows you to split Sublime into panes however you like with simple keyboard shortcuts. You can find my custom key bindings below, which include extensions to Origami's default shortcuts.

#### PackageResourceViewer ####

Enables quick viewing and editing of all your packages. It's a bit shocking that this doesn't come with Sublime by default; without this, you have to manually go through the bowels of your file system to find any `.tmLanguage`, `.sublime-package`, etc. files that you wanted to edit. In contrast, this plugin gives you fuzzy search over all of these packages directly from Sublime. In short –– it's great!

#### Schemr & Themr ####

These two packages enable you to quickly cycle through color schemes and themes (respectively) from any file rather than having to open your preferences file, manually update their file paths, switch back to your original open file to see the changes, and repeat each time you want to test out a new style. These packages aren't so critical for long-term use (I haven't changed my theme in months, and I don't plan on doing so in the near future), but they are really nice when you are first setting up your coding environment.

## Custom key bindings ##

```js
// NOTE: `super` corresponds to `command`
[
  // Utils.
    { "keys": ["super+shift+i"], "command": "reindent"},
    { "keys": ["alt+up"], "command": "move_to", "args": {"to": "bol", "extend": false} },
    { "keys": ["alt+down"], "command": "move_to", "args": {"to": "eol", "extend": false} },

  // Evernote hotkeys.
  { "keys": ["super+shift+o"], "command": "open_evernote_note" },
  { "keys": ["ctrl+super+s"], "command": "save_evernote_note" },
  { "keys": ["ctrl+super+n"], "command": "new_evernote_note" },

  // Open current file in Marked.
  { "keys": ["super+shift+m"], "command": "marked" },

  // Copy path of current file.
  { "keys": ["ctrl+alt+c"], "command": "copy_path" },

  // Origami panes.
  { "keys": ["super+ctrl+n"], "command": "create_pane", "args": {"direction": "down"} },
  { "keys": ["super+ctrl+shift+n"], "command": "create_pane", "args": {"direction": "right"} },
  { "keys": ["super+ctrl+backspace"], "command": "destroy_pane", "args": {"direction": "self"} },

  // Runs tom_doc for currenty ruby function
  { "keys": ["ctrl+d"], "command": "tom_doc" },
]
```

<style type="text/css">
    .gist .highlight, .gist .highlight * {
        font-family: "Inconsolata XL";
        background-color: white !important;
    }
    table tr {
        border: none !important;
    }
</style>