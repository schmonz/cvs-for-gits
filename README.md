# cvs-for-gits

Do you use `git` far more than you use `cvs`? Hopefully that's most of us.

Do you use `cvs` more than zero? Try this drop-in wrapper to make it work a bit more gittishly.

## To install

Copy the script someplace early in `$PATH` (e.g. `$HOME/bin`). Name it `cvs`.

## To use

In general, use `cvs` as usual. (If anything doesn't work as you'd expect or wish, please do me the favor of filing an issue.)

`cvs diff` will colorize and page output just like `git diff`. Make sure you have `colordiff` and `less` installed.
