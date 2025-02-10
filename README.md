# Vim pytest compiler (with traceback support)

## Purpose
This compiler parses all lines of a traceback that contains file paths, so that you can easily
jump up and down the call stack with the usual vim commands that you use to jump through the location list. This is most
useful when looking only at a single test failure (e.g. when pytest is
called with `-x`).

## Installation

Use your favorite vim plugin manager to install `karlb/vim-pytest-traceback` or copy `compiler/pytest.vim` to the directory with you vim compiler files (e.g. `.vim/compiler`).

## Usage

### Plain vim

Enable the compiler with `:compiler pytest`, then run `:make` with any additional parameters you want to pass to pytest.

### dispatch.vim

If you use Tim Pope's [dispatch.vim](https://github.com/tpope/vim-dispatch), the compiler will automatically be used when you use `Dispatch pytest` to run pytest.

### test.vim Configuration
If you use it together with [test.vim](https://github.com/janko/vim-test), you want to
configure pytest to use short tracebacks:
```vim
let test#python#pytest#options = '-Wignore --tb=short -q'
```
