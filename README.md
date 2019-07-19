# Vim pytest compiler (with traceback support)

## Purpose
This compiler file matches all lines of a traceback, so that you can easily
jump up and down the call stack with the usual vim commands. This is most
useful when looking only at a single test failure (e.g. when pytest is
called with `-x`).

## Configuration
If you use it together with [test.vim](https://github.com/janko/vim-test), you want to
configure mypy to use short tracebacks:
```vim
let test#python#pytest#options = '-Wignore --tb=short -q'
```
