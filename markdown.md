GitHub Markdown
===============

Table of Contents
-----------------

* [Text Formatting](markdown.md#eext-formatting)
  * [Blockquote](markdown.md#blockquote)
  * [Bold Text](markdown.md#bold-text)
  * [Emphasis](markdown.md#emphasis)
  * [Italic / Oblique](markdown.md#italic--oblique)
  * [Monospaced / Code Block](markdown.md#monospaced--code-block)
* [Headers and Titles](markdown.md#headers-and-titles)
* [Links](markdown.md#links)
* [Lists and Tables](markdown.md#lists-and-tables)
  * [Task Lists](#task-lists)
* [Other Formatting](markdown.md#other-formatting)
  * [Horizontal Rules](markdown.md#horizontal-rules)
* [Images](markdown.md#images)
* [Footnotes](markdown.md#footnotes)


Text Formatting
---------------

### blockquote

> If you are neutral in situations of injustice, you have chosen the side of the
> oppressor.  If an elephant has its foot on the tial of a mouse and you say that you are neutral, the mouse will not appreciate your neutrality.
Desmont Tutu

```
> If you are neutral in situations of injustice, you have chosen the side of the
> oppressor.  If an elephant has its foot on the tial of a mouse and you say that you are neutral, the mouse will not appreciate your neutrality.
Desmont Tutu
```

### Bold Text

**bold text**

```
**bold text**
```

### Emphasis

words words _emphasized words_ words words

```
words words _emphasized words_ words words
```

### Italic / Oblique

words words *italicized text* words words

```
words words *italicized text* words words
```

### Monospaced / code block

#### Generic (no syntax highlighting)

Designated with three leading back ticks (`) before the block, and three after:

```
#define F_CPU 16000000
#include <avr/io.h>
#include <util/delay.h>

int main(void) {
    DDRB = 0X01; // setup pin 0 on port B
    while (1) // loop forever
    {
        PORTB = 0X01;   // set pin 0 on port B high
        _delay_ms(500);
        PORTB = 0x00;   // set pin 0 on por B low
        _delay_ms(500);
    }
    return 0;
}
```

#### Syntax Highlighting

Follow the three leading backticks with the name of the
[language](https://github.com/github/linguist/blob/master/lib/linguist/languages.yml):

```python
@width.setter
def width(self, value):
    try:
        value = abs(int(value))
    except ValueError:
        print ("Could not convert \"%s\" into an int." %value)
        value = 0
    self.__width = value
```

The opening backticks and code name in that example look like this:

    ```python

#### In-line monospace

To use `monospace` within a paragraph use a single leading and tailing back tick.

```
To use `monospace` within a paragraph use a single leading and tailing back tick.
```

### Paragraphs

Paragraphs are delimited by double carrage returns.

There must be a blank line between paragraphs to designate them as such.
You may add single carage returns so that your text is easier to see (say in
a text editor that is only 80 chars wide), but when this text is interpreted by a GitHub's markdown engine it will be reflowed regardless of line length.

```
Paragraphs are delimited by double carrage returns.

There must be a blank line between paragraphs to designate them as such.
You may add single carage returns so that your text is easier to see (say in
a text editor that is only 80 chars wide), but when this text is interpreted by a GitHub's markdown engine it will be reflowed regardless of line length.
```

### Strike Out

words words ~~strikeout~~ words words

```
words words ~~strikeout~~ words words
```

Headers and Titles
------------------

# H1
## H2
### H3
#### H4
##### H5
###### H6

```
# H1
## H2
### H3
#### H4
##### H5
###### H6
```

Head 1
======

Head 2
------

```
Head 1
======

Head 2
------
```

Links
-----

Links in your [text](http://en.wikipedia.org/wiki/Written_text) can be in-line
with the text and can have optional [mouseover](http://www.w3schools.com/tags/att_img_alt.asp "w3schools rocks!")
attribute.  You can also define [your][1] links later in the [document] by
styling them like a list of [footnotes][2] (this feels like the [markdown] way
of doing things).  (The foot note list can be anywhere in the document, mine is
at the very bottom.)

Lastly, here is a link to the [README file](README.md) in this repo.  Note that
this is a relative link.  If need be you can point out the path with `./` and
`../` type syntax.

```
Links in your [text](http://en.wikipedia.org/wiki/Written_text) can be in-line
with the text and can have optional [mouseover](http://www.w3schools.com/tags/att_img_alt.asp "w3schools rocks!")
attribute.  You can also define [your][1] links later in the [document] by
styling them like a list of [footnotes][2] (this feels like the [markdown] way
of doing things).  (The foot note list can be anywhere in the document, mine is
at the very bottom.)

Lastly, here is a link to the [README file](README.md) in this repo.  Note that
this is a relative link.  If need be you can point out the path with `./` and
`../` type syntax.
```

Links within a document are also supported.  Note that
* spaces are replaced with dashes (`-`).
* all chars are lower case.
* special characters like `/` are omitted.

Here is the code for the (incomplete) table of contents at the top of this page:

```
* [Text Formatting](markdown.md#eext-formatting)
  * [Blockquote](markdown.md#blockquote)
  * [Bold Text](markdown.md#bold-text)
  * [Emphasis](markdown.md#emphasis)
  * [Italic / Oblique](markdown.md#italic--oblique)
  * [Monospaced / Code Block](markdown.md#monospaced--code-block)
* [Headers and Titles](markdown.md#headers-and-titles)
* [Links](markdown.md#links)
* [Lists and Tables](markdown.md#lists-and-tables)
* [Other Formatting](markdown.md#other-formatting)
  * [Horizontal Rules](markdown.md#horizontal-rules)
* [Images](markdown.md#images)
* [Footnotes](markdown.md#footnotes)
```

### Special GitHub links

This example take from [here](https://help.github.com/articles/github-flavored-markdown#references)

* SHA: 16c999e8c71134401a78d4d46435517b2271d6ac
* User@SHA: mojombo@16c999e8c71134401a78d4d46435517b2271d6ac
* User/Repository@SHA: mojombo/github-flavored-markdown@16c999e8c71134401a78d4d46435517b2271d6ac
* #Num: #1
* User#Num: mojombo#1
* User/Repository#Num: mojombo/github-flavored-markdown#1

```
* SHA: 16c999e8c71134401a78d4d46435517b2271d6ac
* User@SHA: mojombo@16c999e8c71134401a78d4d46435517b2271d6ac
* User/Repository@SHA: mojombo/github-flavored-markdown@16c999e8c71134401a78d4d46435517b2271d6ac
* #Num: #1
* User#Num: mojombo#1
* User/Repository#Num: mojombo/github-flavored-markdown#1
```

Lists and Tables
----------------

### Bulleted Lists

* item 1
* item 2
* deeper indentation not supported
- and you can use other symbols
+ in place of the asterisks
  * bulleted lists can have child lists too
  * you just have to manually indent them with two spaces
* Lots of different things going on in this list
 * what happens if you only indent by one space?

```
* item 1
* item 2
* deeper indentation not supported
- and you can use other symbols
+ in place of the asterisks
  * bulleted lists can have child lists too
  * you just have to manually indent them with two spaces
* Lots of different things going on in this list
 * what happens if you only indent by one space?
```

### Numbered List

1. First item in the parent list.
  1. first item in the child list.
    1. What if I want a grandchild in a numbered list.
  2. second item in the child list.
  1. you don't even have ot use the coorect numbers!
  * unnumbered item in the child list gets numbered anyhow.
   * but its child list doesn't.
  - each level of a list has uniform numbering.
2. A line on a list can actually be broken into multiple paragraphs.

   You just need to manually indent the second paragraph so that it is aligned with the first, then you need to include a blank line - see the section on paragraph styling in this document.

3. Then you continue with the list as usual.

```
1. First item in the parent list.
  1. first item in the child list.
    1. What if I want a grandchild in a numbered list.
  2. second item in the child list.
  1. you don't even have ot use the coorect numbers!
  * unnumbered item in the child list gets numbered anyhow.
   * but its child list doesn't.
  - each level of a list has uniform numbering.
2. A line on a list can actually be broken into multiple paragraphs.

   You just need to manually indent the second paragraph so that it is aligned with the first, then you need to include a blank line - see the section on paragraph styling in this document.
3. Then you continue with the list as usual.
```

### Task Lists

(support coming soon?)

- [x] Make cheat-sheet of GitHub markdown
- [x] Upload that cheat-sheat to GitHub
- [ ] Answer a bunch of other questions
- [ ] Achieve world ~~domination~~ peace.

```
- [x] Make cheat-sheet of GitHub markdown
- [x] Upload that cheat-sheat to GitHub
- [ ] Answer a bunch of other questions
- [ ] Achieve world ~~domination~~ peace.
```

### Tables

Tables can be made with the pipe character:

| header 1 | header 2 |
| --- | --- |
|left | right|
| center | `other style` |
|column  |is aligned     |
no outter |pipes

```
| header 1 | header 2 |
| --- | --- |
|left | right|
| center | `other style` |
|column  |is aligned     |
no outter |pipes
```

Other Formatting
----------------

### Horizontal Rules

Three minus-signs(-), asterisks (*), or underscores (_).

---

***

___

```
---

***

___
```

Images
------

![alt attribute 1](http://sagacious.us/sandbox/sandbox.png "hover text (optional - but recomended by web standards)")

![alt attribute 1][href of image]

```
![alt attribute 1](http://sagacious.us/sandbox/sandbox.png "hover text (optional - but recomended by web standards)")

![alt attribute 1][href of image]
```

Footnotes
---------

These were described earlier (under the section on links, they aren't usually
visible when a `.md` file is parsed - you'll need to hit the button at the top 
of this page to see how that works.

  [1]: http://www.grammar-monster.com/easily_confused/youre_your.htm
  [2]: http://en.wikipedia.org/wiki/Footnote "Wikipedia article on notes"
  [document]: http://en.wikipedia.org/wiki/Document
  [markdown]: http://en.wikipedia.org/wiki/Markdown
  [href of image]: http://sagacious.us/sandbox/sandbox.png "hover text"
