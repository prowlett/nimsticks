# nimsticks: LaTeX package for drawing Nim sticks and games

nimsticks is a package for LaTeX that should also work with LuaTeX and XeTeX, that draws sticks for representating games of multi-pile Nim.

By [Peter Rowlett](https://github.com/prowlett/).

## Background

Nim objects could be anything, of course, but conventionally sticks or stones are used. There are various types of dot in LaTeX that might look like stones, but somehow a line of dots didn't seem satisfactory. There are various ways to draw a line (e.g. just typing IIIII), including some tally markers (e.g. in hhcount). My problem with these (call me picky) is that they are all identical lines, and a `heap' of them just looks very organised. Really, I want a set of lines that looks like someone just threw them into heaps (though probably without crossings for the avoidance of ambiguity).

The way this works is it draws a thick vertical line in TikZ with a little wobble added so each one doesn't look extremely well-lined-up with its neighbour, achieved by adding or subtracting a small random number to the top and bottom coordinate.

It does this by providing two commands:

- `\drawnimstick`: draws a single Nim stick with a little random wobble;
- `\nimgame`: takes a comma-separated list of numbers and draws a line of Nim heaps holding those number of sticks.

## Licensing
This work may be distributed and/or modified under the conditions of the [MIT license](LICENSE.txt).

## Changes

### [1.2] - 2022-08-09

- Switched `ifthen` to `etoolbox`;
- Switched `\begin{center}` to `\centering` (because the former doesn't work in `standalone` documents and the latter doesn't add vertical space);
- Removed some whitespace that appeared to the right of the last heap.

### [1.1] - 2020-07-19

- Added option to create inline Nim game using `\nimgame[inline]{}`.
- Added this and made other minor tweaks to documentation.

### [1.0.1] - 2020-07-12

- Fixed typo in usage example in documentation.

### [1.0] - 2020-07-12

- First working version of package
- Added \drawnimstick and \nimgame using lcg for the random numbers so it works across LaTeX, LuaTeX and XeTeX
- Added documentation
