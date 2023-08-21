# Markdown  Reference

The purpose of this tutorial is to introduce you to markdown in Jupyter Notebook.

Many parts of this page are quoted verbatim from the [Jupyter Notebook Users Manual](https://athena.brynmawr.edu/jupyter/hub/dblank/public/Jupyter%20Notebook%20Users%20Manual.ipynb) by Doug Blank at Bryn Mawr College.

----

## <a name="headings"></a>Headings

To make a Level 1 Heading (the largest font), type 

```
    # My Heading 1
```

which displays as:

# My Heading 1

To view the results, type *shift-enter*.

For a second-level header, use

```
    ## My Heading 2
```

which will appear as:

## My Heading 2

Others are:

```
    ### My Heading 3
```

### My Heading 3

```
    #### My Heading 4
```

#### My Heading 4

```
    ##### My Heading 5
```

#### My Heading 5

```
    ###### My Heading 6
```

###### My Heading 6

In these examples, the hashtags are markers which tell the Notebook how to typeset the text. (The space after the hashtags is required.) There are many markup languages with the most familiar being HTML (Hyper Text Markup Language).

One markup language is called **Markdown**, named somewhat jokingly for its simplicity. Markdown is a plain text formatting syntax that Jupyter uses to generate HTML, which the cell can interpret and render. This means that Markdown Cells can also render plain HTML code. If you're interested in learning HTML, check out this [helpful online tutorial][html tutorial].

This [Github-flavored Markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) page has many useful links.

[html tutorial]: http://www.w3schools.com/html/ "w3schools.com HTML Tutorial"

----

## <a name="lists"></a>Lists

In Markdown, you can list items using numbers, a **`+`**, a **` - `**, or a **`*`**. However, if the first item in a list or sublist is numbered, Markdown will interpret the entire list or sublist as ordered and will automatically number the items linearly, no matter what character you use to denote any given separate item.

```
####Sports Teams:

1. St. Louis
    1. Cardinals
    - Blues

- Philadelphia
    1. Eagles
    - Phillies
    - Sixers
    - Flyers

- Chicago
    1. Cubs
    - White Sox
    - Bears
    * Blackhawks
    + Bulls
``` 

#### Sports Teams:

1. St. Louis
    1. Cardinals
    - Blues

- Philadelphia
    1. Eagles
    - Phillies
    - Sixers
    - Flyers

- Chicago
    1. Cubs
    - White Sox
    - Bears
    * Blackhawks
    + Bulls

For a bulleted list, do not begin with a number.

```
####Sports Teams:

* St. Louis
    - Cardinals
    - Blues

- Philadelphia
    * Eagles
    - Phillies
    - Sixers
    - Flyers

- Chicago
    + Cubs
    - White Sox
    - Bears
    * Blackhawks
``` 

#### Sports Teams:

* St. Louis
    - Cardinals
    - Blues

- Philadelphia
    * Eagles
    - Phillies
    - Sixers
    - Flyers

- Chicago
    + Cubs
    - White Sox
    - Bears
    * Blackhawks

----

## <a name="links"></a>Hyperlinks

### Automatic Links

```
http://en.wikipedia.org
```

http://en.wikipedia.org

### Standard Links

```
[click this link](http://en.wikipedia.org)
```

[click this link](http://en.wikipedia.org)

----

## <a name="styles"></a>Style and Emphasis

```
*Italics*
```

*Italics*

```
_Italics with underscores_
```

_Italics with underscores_

```
**Bold**
```

**Bold**

```
__Bold with double underscores__
```

__Bold with double underscores__

**Note:** If you want actual asterisks or underscores to appear in your text, you can use the backslash escape function like this:

```
\*awesome asterisks\* and \_incredible under scores\_
```

\*awesome asterisks\* and \_incredible under scores\_

----

## <a name="math"></a>LaTeX for Mathematical Typesetting

Jupyter Notebooks' Markdown cells support LaTeX for formatting mathematical equations. To tell Markdown to interpret your text as LaTeX, surround your input with dollar signs like this:

```
This equation $z=\dfrac{2x}{3y}$ is in a sentence.
```

This equation $(z=\dfrac{2x}{3y})$ is in a sentence.

An equation can be very complex:

```
$$F(k) = \int_{-\infty}^{\infty} f(x) e^{2\pi i k} dx$$
```

$$F(k) = \int_{-\infty}^{\infty} f(x) e^{2\pi i k} dx$$

If you want your LaTex equations to be indented towards the center of the cell, surround your equation with two dollar signs on each side like this: 

```
$$2x+3y=z$$
```

$$2x+3y=z$$

----
## <a name="tables"></a>Tables

In Markdown, you can make a table by using vertical bars and dashes to define the cell and header borders:

```
|Header|Header|Header|Header|
|------|------|------|------|
|Cell 11 |Cell 12 |Cell 13 | Cell 14|
|Cell 21 |Cell 22 |Cell 23 | Cell 24|
|Cell 31 |Cell 32 |Cell 33 | Cell 34|
|Cell 41 |Cell 42 |Cell 43 | Cell 44|
```

|Header|Header|Header|Header|
|------|------|------|------|
|Cell 11 |Cell 12 |Cell 13 | Cell 14|
|Cell 21 |Cell 22 |Cell 23 | Cell 24|
|Cell 31 |Cell 32 |Cell 33 | Cell 34|
|Cell 41 |Cell 42 |Cell 43 | Cell 44|

### Cell Justification

If not otherwise specified, the text in each header and cell of a table will justify to the left. If, however, you wish to specify either right justification or centering, you may do so like this: 

```
centered header  |  regular header  |  right-justified header  |  centered header  |  regular header  
:---:|---|---:|:---:|---
centered cell|regular cell|right-justified cell|centered cell|regular cell
centered cell|regular cell|right-justified cell|centered cell|regular cell
```

centered header  |  regular header  |  right-justified header  |  centered header  |  regular header  
:---:|---|---:|:---:|---
centered cell|regular cell|right-justified cell|centered cell|regular cell
centered cell|regular cell|right-justified cell|centered cell|regular cell


While it is difficult to see that the headers are differently justified from one another, this is just because the longest line of characters in any column defines the width of the headers and cells in that column. 

**Note:** You cannot make tables directly beneath a line of text. You must put a blank line between the end of a paragraph and the beginning of a table. 

----

## <a name="code"></a>Including Code Examples

If you want to signify that a particular section of text is actually an example of code, you can use backquotes to surround the code example. These will switch the font to monospace, which creates a clear visual formatting difference between the text that is meant to be code and the text that isn't. 

Code can either in the middle of a paragraph, or as a block. Use a single backquote to start and stop code in the middle of a paragraph. Here's an example:

```
The word `monospace` will appear in a code-like form.
```

The word `monospace` will appear in a code-like form.

To include a complete code-block inside a Markdown cell, use triple backquotes. Optionally, you can put the name of the language that you are quoting after the starting triple backquotes, like this:

<pre>
\```python
def function(n):
    return n + 1
\```
</pre>

That will format the code-block (sometimes called "fenced code") with syntax coloring. The above code block will be rendered like this:

```python
def function(n):
    return n + 1
```

The language formatting names that you can currently use after the triple backquote are:

```
apl           django   go            jinja2      ntriples    q       smalltalk    toml
asterisk      dtd      groovy        julia       octave      r       smarty       turtle
clike         dylan    haml          less        pascal      rpm     smartymixed  vb
clojure       ecl      haskell       livescript  pegjs       rst     solr         vbscript
cobol         eiffel   haxe          lua         perl        ruby    sparql       velocity
coffeescript  erlang   htmlembedded  markdown    php         rust    sql          verilog
commonlisp    fortran  htmlmixed                 pig         sass    stex         xml
css           gas      http          mirc        properties  scheme  tcl          xquery
d             gfm      jade          mllike      puppet      shell   tiddlywiki   yaml
diff          gherkin  javascript    nginx       python      sieve   tiki         z80
```

----

## <a name="images"></a>Images

### Images from the Internet

Inserting an image from the internet is almost identical to inserting a link. You just also type a **`!`** before the first set of brackets:

```
![Type anything here](http://www.glowscript.org/docs/GlowScriptDocs/images/cover.jpg "GlowScript Program")
```

![Type anything here](http://www.glowscript.org/docs/GlowScriptDocs/images/cover.jpg "GlowScript Program")

**Note:** The words that you type in the first set of brackets do not appear when they are rendered into html by Markdown. The words within quotes will appear when you hover and pause over the image with your mouse.

----

## <a name="special"></a>Special Characters

What happens if you want to include a literal character, like a **`#`**, that usually has a specific function in Markdown? Backslash Escape is a function that prevents Markdown from interpreting a character as an instruction, rather than as the character itself. It works like this:

```
\# Wow, this isn't a header. 
# This is definitely a header.
```

\# Wow, this isn't a header. 
# This is definitely a header.

Markdown allows you to use a backslash to escape from the functions of the following characters:
* \   backslash
* `   backtick
* \*   asterisk
* _   underscore
* {}  curly braces
* []  square brackets
* ()  parentheses
* \#   hashtag
* \+   plus sign|
* \-   minus sign (hyphen)
* .   dot
* !   exclamation mark