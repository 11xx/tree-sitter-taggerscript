# tree-sitter-taggerscript

Tree-sitter grammar for MusicBrainz Picard Tagger Script.

## Install

For local development, install `tree-sitter-cli` and keep `tree-sitter` on
`PATH`.

For Emacs, use `treesit-install-language-grammar` with:

`https://codeberg.org/useless-utils/tree-sitter-taggerscript.git`

## Build

```bash
npm install
npm test
```

## Scanner

`src/scanner.c` handles `$noop(...)` as opaque content. It tracks balanced
parentheses and emits one external token for the whole noop body, so nested
parentheses inside comments parse correctly without interpreting inner text as
functions or variables.
