# tree-sitter-taggerscript

Tree-Sitter grammar for MusicBrainz Picard Tagger Script.

## Install

### `npm`

> npm install

> npm test

Installs to `$XDG_CACHE_HOME/tree-sitter/lib/taggerscript.so`

### `tree-sitter-cli`

test with

> tree-sitter test

and build with

> tree-sitter build

and it will generate the `.so` file.

`npx` can also be used e.g. `npx tree-sitter test`

### Emacs

For Emacs, use `treesit-install-language-grammar` with:

> https://codeberg.org/useless-utils/tree-sitter-taggerscript

A major mode package https://codeberg.org/useless-utils/picard-mode is also
available and it provides a helper.


## Scanner

`src/scanner.c` handles `$noop(...)` as opaque content. It tracks balanced
parentheses and emits one external token for the whole noop body, so nested
parentheses inside comments parse correctly without interpreting inner text as
functions or variables.

## Credits

This repo is not affiliated with phw's but he made a version years ago:
https://git.sr.ht/~phw/tree-sitter-taggerscript/
