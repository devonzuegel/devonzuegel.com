## Misc Tools ##

* Batch converting `.erb` files to `.slim` (requires erb2slim and html2slim gems) by recursing through all sub-directories:

```shell
$ for f in **/*.erb; do erb2slim $f ${f/\.erb/.slim}; done
$ rm **/*/erb
```

* [Emmet.io](http://docs.emmet.io/) is a toolkit that allows you to expand css-like abbreviations to markup. For example, when you press `TAB` it dynamically parses this...:

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

* [JSON Formatter](https://chrome.google.com/webstore/detail/json-formatter/bcjindcccaagfpapjjmafapmmgkkhgoa?hl=en) enables syntax highlighting and collapsible trees with indent guides when working with raw JSON in your browser. One of my favorite features is that holding down `cmd` while collapsing a subtree collapses all of its siblings, too.

  <div class='space'></div>
  ![](https://lh6.googleusercontent.com/68vofGty-EmFi1WHH-y0IbwRXeJpKTg3eTZOjZQoZAhJ6vuY7cL0G6yJ0CsE5sooUtJkSbqwUbI=s1280-h800-e365-rw)