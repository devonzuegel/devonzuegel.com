# Personal Site

## Getting started

One-time installation:

```sh
npm i -g docpad
npm i
docpad install jade
docpad install markdown # TODO: maybe unnecessary?
docpad install less
docpad install marked
docpad install moment
```

Then to run with livereload:

```
docpad run
```

## Misc

### Run LiveReload

1. `cd` into the project directory (`./devonzuegel.com`)
2. Execute `$ docpad run`, and visit `http://localhost:9778/` to view the
   live-reloading site.

## Q&A

**Q:** _I've installed a plugin, but it doesn't appear to be doing anything!_

Try cancelling the running site and executing `$ docpad run` once again. The
`package.json` file doesn't live-reload on save.
