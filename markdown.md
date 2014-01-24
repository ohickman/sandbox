Big Headers with Equal sign
===========================
Sub headers with minus
----------------------

# H1
## H2
### H3
#### H4
##### H5
###### H6


~~strikethrough~~
**bold** double astrisks
`monospace` uses back ticks
*Italic* sing asterisks
_another italic (emphasis)_ single underscore
__under score__ double underscore

an em---dash is just three minus chars.
Horizontal rules have a space before and after and can be made like these:

---

***

___

> block quotes are designated with brackets
> but the text doesn't re-flow.

> What if I have a really long quote?  Will it _reflow_ into multiple lines?  Did you know that "taco cat" is a palindrome?  It is.

Code block
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

    @width.setter
    def width(self, value):
        try:
            value = abs(int(value))
        except ValueError:
            print ("Could not convert \"%s\" into an int." %value)
            value = 0
        self.__width = value

Tables get headers by using a horizontal rule markup
| header 1 | header 2 |
| --- | --- |
|left | right|
| center | `other style` |
|column  |is aligned     |
no outter |pipes

Paragraphs are delimited by double carrage returns.

So there is a blank line in your source text and there is a blank line in the final document.
But if you want the paragraphs butted up against eachother, that is OK too.

Task List
* [ ] not complted
* [x] completed
[ ] not completed
[x] completed

Bulleted List
* item 1
* item 2
* deeper indentation not supported
- and you can use other symbols
+ in place of the asterisks

Numbered List
# first item
# second item
# nested lists not supported

Manually nubered list
1. first item
2. second item
3. third item is multiple lines long.
   Aparently there is more to say about this item than there was about the others.

Perhaps there are sub-lists:
1. First item in the parent list.
  1. first item in the child list.
    1. What if I want a grandchild in a numbered list.
  2. second item in the child list.
  1. you don't even have ot use the coorect numbers!
  * unnumbered item in the child list.
   * deeper unnumberd item is a grandchild.

Some HTML can be used in GitHub's markdown
    <pre>
    <div>
    <table>, <tr>, <td>, <th>
    
Images
![alt attribute 1](http://sagacious.us/sandbox/sandbox.png "alt attribute 2")
![alt attribute 1][href of image]


Links in your [text](http://en.wikipedia.org/wiki/Written_text) are also possible, you can even have [hover text](http://en.wikipedia.org/wiki/Mouseover "Mouseover").

Links as foot notes
In my text I might make a [claim] [1] that needs to be supported with a [link] [2] to something.  So I put the foot note call outs where they need to be and I add a list at the bottom of the page (or just about anywhere else in the .md document) that supplies the href for the citations.  Perhaps you don't [want a number].

  [1]: http://en.wikipedia.org/wiki/Proposition
  [2]: http://en.wikipedia.org/wiki/Hyperlink
  [want a number]: http://www.example.com
  [href of image]: http://sagacious.us/sandbox/sandbox.png "alt attribute 2"
