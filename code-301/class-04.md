# Responsive Web Design and Regular Expressions


To get started you have to define a container element as a grid with display: grid, set the column and row sizes with grid-template-columns and grid-template-rows, and then place its child elements into the grid with grid-column and grid-row.. Similarly to flexbox, the source order of the grid items doesn’t matter. Your CSS can place them in any order, which makes it super easy to rearrange your grid with media queries.



### Properties for the Grid Container

-   `  display: grid | inline-grid;`
-   `grid-template-columns` `grid-template-rows`

```css
.container {
    /*names are optional*/
    /*line can have more than one name, written in the sampe brace and seperated b spaces*/
  grid-template-columns: [first] 40px [line2] 50px [line3] auto [col4-start] 50px [five] 40px [end];
  grid-template-rows: [row1-start] 25% [row1-end] 100px [third-line] auto [last-line];
}
/*also use the repeat() function*/
  grid-template-columns: repeat(3, 20px [col-start]);
```
The `fr` unit allows you to set the size of a track as a fraction of the free space of the grid container.

-   `grid-template-areas` values - `<grid-area-name>` `.` `none`

-   `grid-template` A shorthand for setting `grid-template-rows`, `grid-template-columns`, and `grid-template-areas` in a single declaration.

-   `  column-gap: <line-size>;`
  `row-gap: <line-size>;`

-   `justify-items`
Aligns grid items along the inline (row) axis (as opposed to align-items which aligns along the block (column) axis)


### Properties for the Grid Items

-   `grid-column` and `grid-row` values-`<start-line> / <end-line>`

-   `grid-area` Gives an item a name.

-   `justify-self` `align-self`

## REGEX (Regular Expression)

used for extracting information from any text by searching for one or more matches of a specific search pattern

-   Anchors — ^ and $
    -   ^: start with
    -   $: end with
    -   `^<text>$`: start AND end with

-   OR operator — | or []
    -   a(b|c) : a then b or c

**Flags**

`/abc/<character(s)>`

-   g (global) does not return after the first match, restarting the subsequent searches from the end of the previous match
-   m (multi-line) when enabled ^ and $ will match the start and end of a line, instead of the whole string
-   i (insensitive) makes the whole expression case-insensitive 

#### CheatSheet
```
Character classes

.	any character except newline
\w\d\s	word, digit, whitespace
\W\D\S	not word, digit, whitespace
[abc]	any of a, b, or c
[^abc]	not a, b, or c
[a-g]	character between a & g
Anchors
^abc$	start / end of the string
\b\B	word, not-word boundary

Escaped characters

\.\*\\	escaped special characters
\t\n\r	tab, linefeed, carriage return

Groups & Lookaround

(abc)	capture group
\1	backreference to group #1
(?:abc)	non-capturing group
(?=abc)	positive lookahead
(?!abc)	negative lookahead

Quantifiers & Alternation

a*a+a?	        0 or more, 1 or more, 0 or 1
a{5}a{2,}	exactly five, two or more
a{1,3}	        between one & three
a+?a{2,}?	match as few as possible
ab|cd	        match ab or cd
```




