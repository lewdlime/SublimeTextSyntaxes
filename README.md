# SublimeTextSyntaxes
Syntax definitions for various languages &amp; markups.

Included syntax definitions:

* **ABC Notation**: ABC Music Notation, a widely used text-based music notation system.
* **RELAX NG Compact**: Used for defining XML schema in a non-XML format.
* **Augmented BNF**: Parser definition language. Used to describe the terminal rule syntax of standardized programming languages and markup languages. Features of this language differ from the original form of BNF. [See here for more info.](https://tools.ietf.org/rfc/rfc5234.txt)
* **Extended BNF**: Parser definition language. Used to describe the terminal rule syntax of standardized programming languages and markup languages. Features of this language differ from the original form of BNF. [See here for more info.](http://www.cl.cam.ac.uk/~mgk25/iso-14977.pdf)

## Notes About ABC Notation:

ABC Commands / Directives have a number of scopes relative to what they do, and how they are intended to be used:

1. **Global**: Scope of the whole ABC file
2. **Page**: Scope of the current page
3. **Tune**: Scope of the current tune
4. **Voice**: Scope of the current voice
5. **Immediate**: Scope of the next immediate note
6. **Generation**: Scope of the next immediate group of notes
7. **Restart**: Command has no scope, but acts as a placeholder for where other command's scopes may be forced to reset, as if a new tune was begun.

If using the syntax highlighting scheme as a basis for plugins to build off of, keep these scopes in mind.

### Operator Overloads

From a syntax standpoint, ABC Notation is very notorious for operator overloading, but with good enough reason to forgive it for doing so. If it didn't, the notation syntax probably wouldn't be as readable to human composers.

None the less, it should be important to indicate that ABC Notation considers chords as individual notes on their own. The `[` and `]` characters that start and end a chord are **NOT** multiline sections, even if they seem to look like such. The same applies to grace notes, which use `{` and `}`, and even has a distinction of how text annotations and accompaniment chords form, despite that they both start with `"`.

### ABC Is **NOT** Markup

ABC Notation is **NOT** a markup language. If it was, it would only be limited to using strictly markup scopes, and would be limited to only the complexity needed to format content on a webpage or a piece of paper. But languages like Markdown exist, as do systems like . Additionally, there are multiple commands that support embedded PROGRAMMING language scopes within ABC Notation files:

* `%%beginjs ... %%endjs`: JavaScript Code (abc2svg / abcjs)
* `%%beginps ... %%endps`: PostScript Code
* `%%beginsvg ... %%endsvg`: SVG [XML] Content
* `%%beginml ... %%endml`: HTML / Generic Markup Language Content
* `%%beginmd ... %%endmd`: Markdown Content
* `%%begintext ... %%endtext`: Optionally formatted text Content

This aside, ABC Notation can't count as a markup language, namely because of how expressive and syntax oriented it is. Additionally, in neither HTML or Markdown can you redefine tags or symbols. In ABC Notation, you can, and you can even add macros, or signify preprocessor statements, for abcpp. The nail in the coffin on this is that markup languages don't have preprocessors, they have rendering engines. ABC doesn't have a rendering engine because it will never conform to a markup language's lexicon: Music notation is a syntactical language, NOT a document format, nor is it a markup in between a formatted page and code. Music notation IS code: You have to learn it to be able to read and write it. **There are many who will say that music notation is a markup, & they will always be wrong: Music is a language _first_, a performance _second_, and a document format _LAST_.**


