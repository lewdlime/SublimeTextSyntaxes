# SublimeTextSyntaxes

Syntax definitions for various languages &amp; markups.

Included syntax definitions:

* **ABC Notation**: ABC Music Notation, a widely used text-based music notation system.
* **GoCoEdit**: Used for the iOS programming editor app, [GoCoEdit](http://gocoedit.com/), for easier editing of it's custom modes & custom themes. _GoCoEdit **is** compatable with SublimeText snippets in XML format._
* **RELAX NG Compact**: Used for defining XML schema in a non-XML format.
* **Augmented BNF**: Parser definition language. Used to describe the terminal rule syntax of standardized programming languages and markup languages. Features of this language differ from the original form of BNF. [See here for more info.](https://tools.ietf.org/rfc/rfc5234.txt)
* **Extended BNF**: Parser definition language. Used to describe the terminal rule syntax of standardized programming languages and markup languages. Features of this language differ from the original form of BNF. [See here for more info.](http://www.cl.cam.ac.uk/~mgk25/iso-14977.pdf)

## Notes About Syntaxes and Themes

This repository contains syntax definitions for both Sublime Text & TextMate-compatible editors. The TextMate-compatible syntaxes are a back-port of the Sublime Text syntax definitions, as the format & system used for Sublime Text's `sublime-syntax` files far outperforms that of TextMate-based syntax definitions, _in my opinion_.

## ABC Notation Notes: _ABC Is **NOT** Markup_

ABC Notation is **NOT** a markup language, despite how it may be considered as such. If it was, it would only be limited to using strictly markup scopes, and would be limited to only the complexity needed to format content on a webpage or a piece of paper. But languages like Markdown exist, as do systems like . Additionally, there are multiple commands that support embedded PROGRAMMING language scopes within ABC Notation files:

* `%%beginjs ... %%endjs`: JavaScript Code (abc2svg / abcjs)
* `%%beginps ... %%endps`: PostScript Code
* `%%beginsvg ... %%endsvg`: SVG [XML] Content
* `%%beginml ... %%endml`: HTML / Generic Markup Language Content
* `%%beginmd ... %%endmd`: Markdown Content
* `%%begintext ... %%endtext`: Optionally formatted text Content

This aside, ABC Notation can't count as a markup language, namely because of how expressive and syntax oriented it is. As the person who had to figure out how to rework the syntax definition from the ground up, I can tell you first hand that anyone calling ABC Notation a "markup" needs a slap to the back of the head.

**There are many who will say that music notation is a markup, & they will always be wrong: Music is a language _first_, a performance _second_, and a document format _LAST_.**

## ToDos:

- [ ] Embed PostScript, SVG, HTML, JavaScript, etc. highlighting within `%%begin...%%end` sections, respectively.
- [ ] Need more snippets, in general. I'd like to have snippets for a large array of scores, from indivual part scores to director score books, and also ABC tunes templates that are configured for specific genres / nationalities of music (Irish reels/jigs/hornpipes, Scottish strathspeys, polka, ballads, jazz, blues, church-oriented hymns, Christmas styled tunes, etc.), as well as for various types of instrumentation templates (piano accompaniments, drumset solos, percussion ensembles, individual sections of orchestras, etc.). Music _is_ the only language that doesn't discriminate.
- [ ] I'd **really** like to advance the ABC Notation into a robust plugin, with features that allow for the best scorewriting capacity available to anyone using ABC Notation: drum mapping, voice & part mapping / management, drum pattern sequencing, etc.
