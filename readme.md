##D3 Handwriting type generator##

Have you ever noticed those [types](http://www.google.com/fonts/specimen/Rock+Salt) that make you think like they are handwritten, only to find same-letter multiples together and have the illusion completely shattered?

With static types, there are simply no satisfactory replacements for a handwritten type. I find that completely upending, and to scratch that itch I've turned to D3 for a more 'proper' implementation of an actual 'handwritten' typeset - one that changes upon rendering.

![](https://raw.githubusercontent.com/maxArturo/d3_handwriting/master/d3_handwriting.gif)

D3 takes care of generating SVG lines for the glyphs, whose coordinates are randomized runtime and interpolated using [basis interpolation](https://en.wikipedia.org/wiki/B-spline) to achieve that good ol' scrawl feel. It also (almost) guarantees that every rendering will be unique - just like every scribble is.


It is worthwhile to note that this is completely preposterous to use as an actual typeface, as it would require JavaScript upon any given display (say, your birthday card). However, this does lend itself to more meaningful applications, such as rendering and then transferring to static media (PDF, say) multiple times over.

I am looking for a proper glyph implementation - one that can be projected and transformed. My current process (painting a glyph with my mouse on the SVG element and saving the coordinates) is not close to optimal, but it works for now. If anyone knows of a better standard way (taking a standard Unicode implementation and parsing out to a SVG:line) do let me know.
