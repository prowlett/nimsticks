# nimsticks: LaTeX package for drawing Nim sticks and games

nimsticks is a package for LaTeX that should also work with LuaTeX and XeTeX, that draws sticks for representating games of multi-pile Nim.

By [Peter Rowlett](https://github.com/prowlett/).

## Background

Nim objects could be anything, of course, but conventionally sticks or stones are used. There are various types of dot in LaTeX that might look like stones, but somehow a line of dots didn't seem satisfactory. There are various ways to draw a line (e.g. just typing IIIII), including some tally markers (e.g. in hhcount). My problem with these (call me picky) is that they are all identical lines, and a `heap' of them just looks very organised. Really, I want a set of lines that looks like someone just threw them into heaps (though probably without crossings for the avoidance of ambiguity).

The way this works is it draws a thick vertical line in TikZ with a little wobble added so each one doesn't look extremely well-lined-up with its neighbour, achieved by adding or subtracting a small random number to the top and bottom coordinate.

It does this by providing two commands:

- `\drawnimstick`: draws a single Nim stick with a little random wobble;
- `\nimgame`: takes a comma-separated list of numbers and draws a line of Nim heaps holding those number of sticks.

## How to use

To use, run `tex nimsticks.ins` and then `pdflatex nimsticks.dtx`.

Then look at the file nimsticks.pdf for more on how to use this package.

## Origin

This is an adapted version of something I wrote about in a blog post [LaTeX for typesetting a multi-pile Nim game](https://aperiodical.com/2018/09/latex-for-typesetting-a-multi-pile-nim-game/) at [The Aperiodical](https://aperiodical.com).