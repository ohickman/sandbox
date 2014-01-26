GitHub Flavored Markdown (GFM)
===============

Table of Contents
-----------------

* [Text Formatting](##text-formatting)
  * [Blockquote](#blockquote)
  * [Bold Text](#bold-text)
  * [Emphasis](#emphasis)
  * [Italic / Oblique](#italic--oblique)
  * [Monospaced / Code Block](#monospaced--code-block)
    * [Without Syntax Highlighting](#generic-no-syntax-highlighting)
    * [With Syntax Highlighting](#syntax-highlighting)
    * [Inline with text](#in-line-monospace)
  * [Paragraphs](#paragraphs)
  * [Strike Out](#strike-out)
* [Headers and Titles](#headers-and-titles)
* [Links](#links)
* [Lists and Tables](#lists-and-tables)
  * [Task Lists](#task-lists)
* [Images](#images)
* [Other Formatting](#other-formatting)
  * [Horizontal Rules](#horizontal-rules)
  * [HTML](#html)
* [Footnotes](#footnotes)


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

Double underscores still envoke em so be careful: __init__ will get an emphasis,
but it should probably be written `__init__` anyway.

Things not considered emphasis
* snake_case_words also look like code so no emphasis
* _private() Because there is no closing tag.

```
words words _emphasized words_ words words

Double underscores still envoke em so be careful: __init__ will get an emphasis,
but it shoudl probably be written `__init__` anyway.

Things not considered emphasis
* snake_case_words also look like code so no emphasis
* _private() Because there is no closing tag.
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
@width.setter
def width(self, value):
    try:
        value = abs(int(value))
    except ValueError:
        print ("Could not convert \"%s\" into an int." %value)
        value = 0
    self.__width = value
```

Or, so long as they are set apart as a single [paragraphs](#paragraphs)
the code block can be indicated with four leading spaces

    @width.setter
    def width(self, value):
        try:
            value = abs(int(value))
        except ValueError:
            print ("Could not convert \"%s\" into an int." %value)
            value = 0
        self.__width = value

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
* All [headers](#headers-and-titles) are automatically turned into anchors.
* spaces are replaced with dashes (`-`).
* all chars are lower case.
* special characters are omitted.
  * Actually the list of *allowed* non-alphanumeric characters is just `'` and `_`.
  * Omitted chars are `! @ # $ % ^ & * = + [ { ] } | ; : ' " < > ? \ ~ ,`

Here is the code for the (incomplete) table of contents at the top of this page:

```
* [Text Formatting](##text-formatting)
  * [Blockquote](#blockquote)
  * [Bold Text](#bold-text)
  * [Emphasis](#emphasis)
  * [Italic / Oblique](#italic--oblique)
  * [Monospaced / Code Block](#monospaced--code-block)
    * [Without Syntax Highlighting](#generic-no-syntax-highlighting)
    * [With Syntax Highlighting](#syntax-highlighting)
    * [Inline with text](#in-line-monospace)
  * [Paragraphs](#paragraphs)
  * [Strike Out](#strike-out)
* [Headers and Titles](#headers-and-titles)
* [Links](#links)
* [Lists and Tables](#lists-and-tables)
  * [Task Lists](#task-lists)
* [Images](#images)
* [Other Formatting](#other-formatting)
  * [Horizontal Rules](#horizontal-rules)
  * [HTML](#html)
* [Footnotes](#footnotes)
```

### Special GitHub links

Most of these examples are taken from [here](https://help.github.com/articles/github-flavored-markdown#references),
where they supposedly work, but they don't seem to be working here.

* SHA: 16c999e8c71134401a78d4d46435517b2271d6ac
* User@SHA: mojombo@16c999e8c71134401a78d4d46435517b2271d6ac
* User/Repository@SHA: mojombo/github-flavored-markdown@16c999e8c71134401a78d4d46435517b2271d6ac
* #Num: #1
* User#Num: mojombo#1
* User/Repository#Num: mojombo/github-flavored-markdown#1
* email address: handle@example.com
* URL: http://www.example.com
* URL: www.example.com
* URL: example.com

```
* SHA: 16c999e8c71134401a78d4d46435517b2271d6ac
* User@SHA: mojombo@16c999e8c71134401a78d4d46435517b2271d6ac
* User/Repository@SHA: mojombo/github-flavored-markdown@16c999e8c71134401a78d4d46435517b2271d6ac
* #Num: #1
* User#Num: mojombo#1
* User/Repository#Num: mojombo/github-flavored-markdown#1
* email address: handle@example.com
* URL: http://www.example.com
* URL: www.example.com
* URL: example.com
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
    * lets go deeper
      * we gotta go deeper!
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
    *  but its child list doesn't.
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
    *  but its child list doesn't.
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

| header 1 | header 2 | header 3 | header 4 |
|:---------|:---:| ---:|---|
|left      |center |right |not specified|
|aligned   | columns | or ragged|are ok|
| _same_ |*style*|~as~|`elsewhere` |
don't | need | outter | pipes

```
| header 1 | header 2 | header 3 | header 4 |
|:---------|:---:| ---:|---|
|left      |center |right |not specified|
|aligned   | columns | or ragged|are ok|
| _same_ |*style*|~~as~~|`elsewhere` |
don't | need | outter | pipes
```

Images
------

![alt attribute](http://sagacious.us/sandbox/sandbox.png "hover text (optional - but recomended by web standards)")

![alt attribute][href of image]

```
![alt attribute](http://sagacious.us/sandbox/sandbox.png "hover text (optional - but recomended by web standards)")

![alt attribute][href of image]
```

Other Formatting
----------------

### Horizontal Rules

Three minus-signs(`-`), asterisks (`*`), or underscores (`_`).

---

***

___

```
---

***

___
```

### HTML
Turns out that you can use a lot of [HTML](html.md) in a GFM markdown file.

Footnotes
---------

These were described earlier (under the section on links, they aren't usually
visible when a `.md` file is parsed - you'll need to hit "raw" the button at the
top of this page to see how that works.  Note that indentation doesn't matter,
but bullets do (bullets break the functionality)

[1]: http://www.grammar-monster.com/easily_confused/youre_your.htm
[2]: http://en.wikipedia.org/wiki/Footnote "Wikipedia article on notes"
[document]: http://en.wikipedia.org/wiki/Document
  [markdown]: http://en.wikipedia.org/wiki/Markdown
  [href of image]: http://sagacious.us/sandbox/sandbox.png "hover text"
