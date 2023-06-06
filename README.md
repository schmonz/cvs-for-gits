# CVS for Gits

Do you use `git` far more than you use `cvs`? Do you use `cvs` more than "not at all"? Try this drop-in wrapper to make it a bit more gittish.

## Installation

Two options:

1. Place the script in `/usr/local/bin` (or wherever you usually install programs), then `alias cvs=cvs-for-gits`.
2. Place the script in `$HOME/bin` (or some other place very early in `$PATH`) with the name `cvs`.

## Usage

For most `cvs` subcommands, `cvs-for-gits` simply executes `cvs(1)`, passing along any command-line arguments.

### `cvs diff`

Output is colorized and paged just like `git diff`.
You'll need `colordiff` and `less` installed.
(You might need to configure `colordiff` to use the same colors as `git diff`.)

When you need a plain diff, use `cvs plaindiff`.

### `cvs show`

Colorizes and pages the latest commitdiff.
`cvs show HEAD^` shows the previous one, and `cvs show HEAD~2` the one before that.
You'll need `cvsps` and `less` installed.

### `cvs gitlog`

Lists the commitlogs (oldest first, but skipping ahead to the end).
You'll need `cvsps` and `less` installed.

If newer commits aren't showing up, `cvs gitlog -x` rebuilds the commitlog cache.

## Improvements

If the wrapper interferes with anything you use `cvs` for, that's a bug. I'll also want to hear about `cvs` tasks we might be able to make easier.
