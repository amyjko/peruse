"
This is a quote. I'm using it to test how the outline floats around non-paragraph headers.
" Amy J. Ko, Ph.D.

Welcome to the Peruse example book! This introduction contains all of the features supported by the platform, and explanation of how they work.

Let's go through each of the basic formatting features of book chapters. To begin, let's start with headers, all of which can be indicated by starting a line with the pound symbol #. For example, here's some code that starts a top-level header:

`markdown
# This is a header
`

That will be formatted like this:

# This is a header

You can put as many as three consecutive pounds for subheaders and sub-subheaders. Even though the web supports more than that, I didn't include more than that because readers tend to get overwhelmed by complex document structures. Here are the three different size:

`markdown
# Header
## Subheader
### Sub-subheader
`

# Header
## _Sub_header
### _Subsub_header

There are many ways to format text.

It can be _italic_ by wrapping text with the \_ symbol:

`markdown
It can be _italic_ by wrapping text with the \_ symbol:
`

It can be *bold* by wrapping text with the \* symbol.

`markdown
It can be *bold* by wrapping text with the \* symbol.
`

It can be both *_bold and italic_* by wrapping words with both \* and \_.

`markdown
It can be both *_bold and italic_* by wrapping words with both.
`

It can be in bullet form by starting a line with \*:

`markdown
* Item _1_
* Item _2_
* Item _3_
`

* Item _1_
* Item _2_
* Item _3_

Bullets can be nested by increasing or decreasing the number of \*:

`markdown
* Item _1_
** Item _1.1_
** Item _1.2_
*** Item _1.2.1_
*** Item _1.2.2_
** Item _1.3_
* Item _3_
* Item _4_
`

* Item _1_
** Item _1.1_
** Item _1.2_
*** Item _1.2.1_
*** Item _1.2.2_
* Item _2_
* Item _3_
* Item _4_

It doesn't matter how many \*'s there are exactly, just whether that number is more or less than the bullets before or after it.

It can be in numbered form by staring a line with a number followed by a period:

`markdown
1. Item 1
2. Item 2
3. Item 3
`
1. Item 1
2. Item 2
3. Item 3

The numbers don't have to be in a particular order, they just have to be a number.

`markdown
3. Item 1
22. Item 2
111. Item 3
`
3. Item 1
22. Item 2
111. Item 3

You can nest numbered lists by increasing or decreasing the number of \.'s:

`markdown
1. Item _1_
1.. Item _1.1_
1.. Item _1.2_
1... Item _1.2.1_
1... Item _1.2.2_
2. Item _1.3_
3. Item _3_
4. Item _4_
`

1. Item _1_
1.. Item _1.1_
1.. Item _1.2_
1... Item _1.2.1_
1... Item _1.2.2_
2. Item _1.3_
3. Item _3_
4. Item _4_

It doesn't matter how many \*'s there are exactly, just whether that number is more or less than the bullets before or after it.


You can include [links to content|http://amyjko.com] like this:

`markdown
You can include [links to content|http://amyjko.com].
`

The \| separates the link text from the URL. All links will open new windows.

You can add links to chapters by just using the chapter identifier given in the book's specification. For example, here's a link to [Chapter 1|chapter1].

`markdown
Visit [Chapter 1|chapter1].
`

Chapter links won't open in new windows.

If you link to a chapter that doesn't exist, bad things happen:

`markdown
Visit [a chapter that doesn't exist|doesnotexist].
`

Visit [a chapter that doesn't exist|doesnotexist].

You can include captioned images like the one at the top of this chapter by using this format, indicating the caption, description of the image, credit for the image, and the image file name:

`markdown
|chapter1.jpg|A photograph of Boomy seeking nuzzles|A caption with a reference <ref1>.|Amy J. Ko|
`

|chapter1.jpg|A photograph of Boomy seeking nuzzles|A caption with a reference <ref1>.|Amy J. Ko|

If you cite something that doesn't appear in your book specification's reference list, you'll get an error like this: <thisisanunknowncitation>.

You can also include footnotes{I'm a footnote}:

`markdown
You can also include footnotes{I'm a footnote}{I'm also a footnote}:
`

If you include more footnotes, Peruse will letter them accordingly{I'm also a footnote}.

You can also include YouTube videos by using the same syntax as above, but just including a YouTube video in the URL instead.

`markdown
|https://www.youtube.com/embed/v=317jz-PU7Mg|A video Amy made with her daughter back when Angry Birds was popular.|A YouTube video showing Angry Birds enacted in real life.|Amy J. Ko|
`

|https://www.youtube.com/embed/v=317jz-PU7Mg|A video Amy made with her daughter back when Angry Birds was popular.|A YouTube video showing Angry Birds enacted in real life.|Amy J. Ko|

You can include code by wrapping any text with a backtick \`:

`
This isn't any particular programming language
It's just some English sentences
It just gets formatted in plain text, fixed width format.
` Yes, this is a haiku.

You can put a caption after the backtick.

If you include a language name after the first backtick like this:

`markdown
\`python
two = 1 + 1
if two == 2:
   print "Truth"
\``

Peruse will try to highlight based on that language's syntax.

`python
two = 1 + 1
if two == 2:
   print "Truth"
` Look, syntax highlighting!

Supported languages are listed in [the HighlightJS documentation|https://github.com/highlightjs/highlight.js/blob/master/SUPPORTED_LANGUAGES.md].

You can also include code inline by wrapping things in \`in backticks\`: `if two == 2: print "Truth"`, and by including the language name after the closing backtick, as in `\`if two == 2: print "Truth"\`python`markdown, you can language format inline code: `if two == 2: print "Truth"`python

You can include comments in text by starting a line with the \% symbol:

`markdown
% This is a comment.
`

% This is a comment.

Text in comments won't be visible in the chapter. This is helpful for keeping notes about improvements to make, or rationale for a section of a chapter.

To use any of the special symbols above, place a \\ a before it to mean that you mean the symbol, and not it's special meaning.

`markdown
     Any space at the beginning or end of a
   line, or before or after a line, will be 
            ignored.   
`

     Any space at the beginning or end of a line, or before or after a line, will be ignored.   

The same is true of extra lines before and after paragraphs.

It's also possible to include quotes:

`markdown
"
This is my quote
" Me
`

"
This is my quote
" Me

It's also important to border text with a callout:

`markdown
=
This is my callout
=
`

=
This is my callout
=

And if that's not enough, you can make tables with captions, with each

`markdown
,this,is,[my|dfjdfdf],table
,the, next,row,is
,my,test,is,*_failing_*
this is my caption
`

Which will render like this:

,this,is,[my|dfjdfdf],table
,the, next,row,is
,my,test,is,*_failing_*
this is my caption

Each cell can have inline formatting as in any other paragraph (but you can't put paragraph-level things in cells).

If you start a line with any number of hyphens...

`markdown
---
`

---

You'll get a horizontal rule.

If you use plain "quotes" in a sentence, it will replace them with 'smart' quotes. Quotes that follow a space get a left curly quote; quotes that come before a space get a right curly quote. And single quotes that appear anywhere other than after a space get a right curly single quote for apostrophes. Isn't that cool?

Quotes of things "should be curly".
This should be independent of "where periods are."
This also works for 'single quotes'.
Also independent of 'where periods are.' And what follows. 
This shouldn't break for contractions, including 'those that appear'n in quotes a'nat' or sentences with 'multiple apostrophes'.
This shouldn't break for "things followed by citations"<ref1>.
This shouldn't "break for commas," either.

We will also replace \-\- with em-dashes -- like the one in this sentence.

You can also cite things <ref1,ref2> or just cite one thing <ref3>.

When clicking on something in the index, the index word should be highlighted no matter how many times the index appears in a span of text and regardless of whether the *index word* is formatted.