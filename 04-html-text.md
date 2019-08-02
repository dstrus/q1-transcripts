Further reading:
* [HTML text fundamentals](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/HTML_text_fundamentals) on MDN
* [HTML entities](https://www.w3schools.com/html/html_entities.asp) on w3schools
* [When should one use HTML entities?](https://stackoverflow.com/questions/436615/when-should-one-use-html-entities) on Stack Overflow

Hey, everyone. Welcome to Kenzie Academy. I'm Davey Strus.

We know that HTML documents have a head, containing metadata and links to external files, and a body, where the actual content belongs. Let's look at some of the elements we can use to mark up that content.

At its most basic, HTML contains hypertext—text with links. We can embed other media in our documents, but we should first be sure that we have a reasonable understanding of our options for marking up plain text.

There are certain semantic elements—which is to say, elements that suggest a certain structure or meaning to their contents—that form the foundation of how we mark up text. Headings and paragraphs—things like that.

```html
<p>Content</p>
```

The paragraph element—`<p>`—is often the first element that people learn. Paragraphs are the fundamental building blocks of text content, since we don't have `<word>` and `<sentence>` elements.

When writing a term paper or something like that, you don't just write huge walls of text. At least I hope you don't. You break it up into paragraphs. We should do the same in our HTML.

```html
<p>
  We had everything before us, we had nothing before us, we
  were all going direct to Heaven, we were all going direct
  the other way— in short, the period was so far like the
  present period, that some of its noisiest authorities
  insisted on its being received, for good or for evil, in
  the superlative degree of comparison only.
</p>
```

Just put an opening `<p>` tag at the beginning of the paragraph, and a corresponding closing tag—`</p>`—at the end.

Put a few paragraphs in a row, and you can see how this affects the presentation. Not only does each paragraph start on a new line; there's also space between each paragraph. It's nice and easy to read. It's not all about presentation though. It's also about **semantics** and structure. We mark them up as paragraphs not simply because we want space between them, but because they _are_ paragraphs.

If we want to fine-tune the presentation of our content, we use CSS. Back in the dark times before CSS, people would add empty paragraphs just to space things out. Want some extra space between things? Just throw a couple of empty paragraphs in there!

```html
<p>Some actual content</p>
<p></p>
<p></p>
<p>More content</p>
```

Gross!

Although throwing text inside a paragraph has implications for its default presentation, we do it because the text _is_ a paragraph. The paragraph element has _meaning_. It has semantics. If you just want more space, use CSS.

So what about marking up the text _within_ a paragraph? Can we do that? Can we nest other elements inside a paragraph? Sure! There are some limitations that we'll discuss later, but the short answer is _yes_.

If you want to emphasize a particular bit of text, just use the `<em>` element.

```html
<p>This is <em>really</em> useful!</p>
```

If you wrap it in an `<em>` element, browsers will display text in italics. Screen readers will also place extra emphasis on those words.

If a particular bit of text is extra important, you can use the `<strong>` element to indicate that.

```html
<p>Use <strong>extreme caution</strong>!</p>
```

Browsers display `<strong>` content in bold.

So `<em>` for italics, `<strong>` for bold, right? Well... not necessarily. Use `<em>` for _emphasis_, and `<strong>` for **importance**. Once again, these are semantic elements. Although they have implications for the way text is presented, use them because the meaning fits. There are reasons to italicize text other than for emphasis, after all.

For example, we italicize book titles. `<em>` isn't a good fit for that, so we have the `<cite>` element.

```html
<p>Is that <cite>Dracula</cite>?</p>
```

Here, I'm asking if the book someone is reading is the book _Dracula_. I'm not asking if the person walking by is Dracula himself. Although if I were asking that, I may very well want to emphasize the word _Dracula_. By default, `<cite>` elements are also italicized, but by using `<cite>` you do have the option to use CSS to style them a little differently from text that is merely emphasized. Also, screen readers know that they don't need to place special emphasis on citations.

There are still other reasons to italicize text—for example, foreign words and phrases. So what do we do then? Neither `<em>` nor `<cite>` really fits. Well, for those cases, we have some ancient elements that were originally purely presentational. Historically, these elements had no semantic meaning attached to them. They just changed the way text was rendered: `<i>`, `<b>`, and `<u>`. Italics, bold, and underline, respectively. HTML 5 actually redefined these elements so that they _do_ have semantics, although they feel kind of vaguely defined. `<i>`, for example, means "something that is generally italicized, but for which there is no more appropriate element". A foreign word or phrase, or the scientific name for a species, for example.

```html
<p>
  What a pretty <i>Canis lupis</i>! Anyway, I'll
  have the <i lang="fr">café au lait</i>.
</p>
```

Ooh, look how fancy I am using the `lang` attribute! We learned about that!

Anyway, if you're italicizing something for emphasis, use `<em>`.

```html
<p>That wave was <em>gnarly</em>!</p>
```

If you're italicizing something because it's a title, use `<cite>`.

```html
<p><cite>Frankenstein</cite> is at the library.</p>
```

If you're italicizing something for some other good reason, use `<i>`.

```html
<p>
  Barnum Brown discovered <i>T. rex</i>, but
  Henry Fairfield Osborn named it.
</p>
```

If you're italicizing something because you just like it that way... well, we'll talk about that when we dig into CSS.

Similarly, if you want something to be bold because it's extra-important, use `<strong>`.

<p>
  <strong>Do not</strong> feed
  them after midnight!
</p>

If you want something to be bold for some other good reason, like introducing a vocabulary word, use `<b>`.

```html
<p>In HTML, we use <b>tags</b>.</p>
```

If you want to bold something because you like the way it looks... once again, we'll talk about that when we get to CSS.

As for `<u>`, well... think really hard before underlining something in HTML, because underlines are strongly associated with hyperlinks. But if you have a really good reason, go ahead, but consider using CSS to make sure it looks sufficiently different from the links on the page.

In all of these examples, I nested these elements inside paragraphs. There's no rule that says they _must_ be inside paragraphs. It's just a very common way to use them. Whenever you do nest one element inside another, however, be sure not to get your tags crossed. You can put one element inside another, but you cannot have elements overlap.

```html
<p>Let's read <cite>Pride and</p> Prejudice</cite>!
```

Here, I've put my closing `p` tag before my closing `cite` tag. No good! That's invalid. You can nest elements, but you can't begin an element inside another one, and then end it outside the other one.

What if I just leave off a closing tag?

```html
<p>Let's read <cite>Thud!</p>
```

We've reached the end of the paragraph, so the browser ought to know that's the end of the citation too. It's true that the browser is likely to correctly guess that the citation should be closed before the paragraph, but this markup is definitely invalid. Don't do that!

OK, let's talk about headings for a moment. HTML gives us six levels of headings, using the elements `<h1>` through `<h6>`. `h1` is the top level heading, and `h6` is the lowest level heading. As far as presentation goes, all of the heading elements will typically show up in bold. An `h1` will also be very big. An `h2` will be a little smaller, but still pretty big. An `h3` will be just a little bigger than normal text, and so on.

```html
<h1>HTML Basics</h1>

<h2>Document structure</h2>
<h3>The head</h3>
<h3>The body</h3>

<h2>Marking up text</h2>
<h3>Paragraphs</h3>
<h3>Headings</h3>
```

But once again, these elements have _meaning_. We don't just use them because we want a particular piece of text to be big and bold. We use them because they're headings. Used properly, they'll create a sort of outline for our document. They provide _structure_.

This is a really good idea. It has the effect of breaking up the page visually, making it easy to scan. And screen readers will often present the headings first, giving people the option to read only specific sections, rather than making them sit through every single word on the page just to get to the bit they're interested in. After all, people who read the page visually get to do that.

All right, so what's the deal with line breaks in the markup? Sometimes I put my tags on the same line as the content...

```html
<p>It was the best of times, it was the worst of times.</p>
```

...and sometimes I put them on separate lines.

```html
<p>
  The sea did what it liked, and what it liked was
  destruction. It thundered at the town, and thundered
  at the cliffs, and brought the coast down, madly.
<p>
```

Then I indent the lines in between, and I sometimes put line breaks in the middle of a sentence. And none of that appears to have any effect on the way it's presented. The browser doesn't draw line breaks in the places where I put them in my markup. And it doesn't indent in the places where I indent.

As you might guess, I'm using line breaks and indentation to make my markup more readable. I can do that because of the way HTML handles **whitespace**. Whitespace includes all those invisible characters—spaces, tabs, line breaks, etc. And the way HTML handles those makes it easy for us to write our markup with a focus on readability.

In short, browsers render any amount of whitespace as a single space. Four spaces? Looks like one space. A line break followed by two spaces? Looks like one space. So put in line breaks and indentation to your heart's content. Make it nice and readable. It won't change the way it looks.

But what if you _want_ it to affect the way it looks? What if you want line breaks to appear exactly where you put them, and for things to line up exactly as they do in the markup? Maybe you have a block of code you want to show, or you want to share an e e cummings poem.

We have a special element for such occasions: `<pre>`, for preformatted text.

```html
<pre>
it's
spring
and
   the

      goat-footed

balloonMan   whistles
far
and
wee
</pre>
```

Here's an excerpt from an e e cummings poem, and the browser will render it with the same spacing that I used in the markup, because I used the `<pre>` element. Not only are the line breaks and spaces where I put them; the browser also switches to a monospace font—that is, a font where every character takes up exactly the same amount of space. The sort of font we use in code editors. That makes it possible to line things up vertically.

OK, one last thing about marking up text: HTML entities. Remember those? We had to use them in order to use quotation marks inside attribute values.

```html
<a title="the &quot;About&quot; page">
  About us
</a>
```

Sometimes you need to use characters in your markup that have the potential to be ambiguous or otherwise problematic. In those cases, you can use HTML entities to represent those characters.

For example, what if you need to use a less-than sign in a paragraph?

```html
<p>I <3 HTML</p>
```

I heart HTML. What's wrong with that? It's that _less-than_ symbol. It thinks that's the beginning of a tag! The less-than sign is known as a reserved character, because it has a special meaning in HTML. Better use an HTML entity.

```html
<p>I &lt;3 HTML</p>
```

There we go. HTML entities begin with an ampersand and end with a semicolon. In between is a code that represents a particular character. In this case, `lt` represents the _less-than_ symbol. When we replace a character with an HTML entity, we say that we are **escaping** that character.

What else is a reserved symbol? Well, there's only one other one that you absolutely _must_ escape, and that's the ampersand. You can't just use an ampersand, because that marks the beginning of an HTML entity. The code for an ampersand is `amp`.

```HTML
Abbott &amp; Costello
```

Both single quotes and double-quotes must be escaped under certain circumstances, but if you're not inside a quoted attribute value, you're free to use them as-is.

You might expect the _greater-than_ symbol to cause the same problems as the less-than symbol, but in reality, it doesn't cause any problems, because it only has special meaning when it follows a less-than symbol.

There's one other really common HTML entity: The non-breaking space. If you want multiple spaces in a row, you can't just put in multiple spaces. They'll get collapsed into one! And you may not really want to treat it as preformatted text, complete with a monospace font. You just want an extra space, dang it! For that, we have the non-breaking space: `nbsp`.

```html
Hello there.&nbsp;&nbsp;I put two spaces
after periods, because I'm old.
```

Aside from the fact that they won't collapse into a single space, you'll also never get a line-break where a non-breaking space appears. So if a line gets to be too long and the browser is deciding where to wrap onto the next line, anyplace there's a non-breaking space will be ineligible.

You can use HTML entities for other invisible characters too. In fact, you _can_ use them for _any_ character by using its numeric code. People often use them for hard-to-type characters, like letters from other alphabets, or letters with accents, or even Emoji. But it's actually considered a best practice these days to just put the character directly in your markup, as long as you're using the UTF-8 encoding, which you should be.

```html
I ❤️ HTML
I &#57378; HTML
```

Having the actual character in the markup is much more readable than having an HTML entity in its place. If you want to know how to look up the entity codes for other extended characters, check out the links in this lesson.

OK, got a handle on how to mark up text in HTML? Very good.

Until next time, I'm Davey Strus. Haaaappy hacking!
