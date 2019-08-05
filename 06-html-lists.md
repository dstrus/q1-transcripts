Further reading:
* [HTML lists](https://www.w3schools.com/html/html_lists.asp) on w3schools
* [Unordered lists](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ul) on MDN
* [Ordered lists](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ol) on MDN
* [List items](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/li) on MDN
* [Description lists](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/dl) on MDN

Hey, everyone. Welcome to Kenzie Academy. I'm Davey Strus.

We're making good progress on learning HTML, but our pages are still pretty boring, with just headers and paragraphs, with the occasional bold or italicized phrase. Let's spice things up with some lists. A mild spice, to be sure, but a spice nonetheless.

We're interested in two types of lists: Unordered lists and ordered lists. Both are made up of list items. There's a third kind of list in HTML called a description list, but it is not made up of list items, and just generally isn't all that similar (or nearly as common) as the other two types, so we're going to focus on unordered lists and ordered lists for right now. Feel free to follow the link to read up on description lists on your own though.

Both unordered and ordered lists are made up of list items, and the markup is virtually identical. So what's the difference? Well, it's right there in the name. In an unordered list, the order of the items doesn't matter. You could rearrange the list, and it would still make just as much sense. Now the browser isn't actually going to rearrange it on you unexpectedly, but when deciding which type of list to use, the question to ask is: Is the order of the items meaningful? If it is, then you want an ordered list. Let's look at the markup.

```html
<h1>Films of 1978</h1>

<h2>Highest grossing films (USA)</h2>
<ol>
  <li>Grease</li>
  <li>Superman</li>
  <li>Animal House</li>
  <li>Every Which Way But Loose</li>
  <li>Heaven Can Wait</li>
</ol>

<h2>Best Picture Nominees</h2>
<ul>
  <li>Midnight Express</li>
  <li>Heaven Can Wait</li>
  <li>The Deer Hunter</li>
  <li>Coming Home</li>
  <li>An Unmarried Woman</li>
</ul>
```

On the left is an ordered list, marked up with the `<ol>` element. On the right is an unordered list, `<ul>`. Both are made up of list items, marked up with `<li>`. In the list on the left, the order is significant. These are the top grossing films of the year, in order. In the list on the right, the order doesn't matter. These are the best picture nominees in no particular order.

So how are these presented in the browser?

Now, I'll admit I cheated a little here. I threw in some divs and a little bit of CSS to get the lists to appear side-by-side. Yours will appear one above the other if you copy the HTML that I showed a moment ago. This just makes it easier to examine the difference. Namely, the ordered list is numbered, and the unordered list is bulleted. That stands to reason, right? Since the order matters in the ordered list, numbering makes sense. And in the unordered list, the bullets make it clear that this is, in fact, a list, even if it is in no particular order. So that's the basic difference.

Ordered lists also have a few optional attributes that unordered lists don't have. If you want to start an ordered list at, say, the 6th item, just add `start="6"`.

```html
<h2>Highest grossing films (USA)</h2>
<ol start="6">
  <li>Hooper</li>
  <li>Jaws 2</li>
  <li>Revenge of the Pink Panther</li>
  <li>The Deer Hunter</li>
  <li>Halloween</li>
</ol>
```

Want to list things in reverse order? Use the boolean attribute `reversed`.

```html
<h2>Top 5</h2>
<ol reversed>
  <li>Heaven Can Wait</li>
  <li>Every Which Way But Loose</li>
  <li>Animal House</li>
  <li>Superman</li>
  <li>Grease</li>
</ol>
```

Remember boolean attributes? Their values are optional. If you do include the value, the value should be the same as the name of the attribute. In this case, `reversed="reversed"`.

```html
<h2>Top 5</h2>
<ol reversed="reversed">
  <li>Heaven Can Wait</li>
  <li>Every Which Way But Loose</li>
  <li>Animal House</li>
  <li>Superman</li>
  <li>Grease</li>
</ol>
```

You can also change the numbering to use uppercase or lowercase letters or Roman numerals, using the `type` attribute.

```html
<h1>Roger Ebert's Grease review</h1>
<ol type="I">
  <li>Introduction</li>
  <li>Cast</li>
  <li>Plot summary</li>
  <li>Strengths</li>
  <li>Weaknesses</li>
  <li>Conclusion</li>
</ol>
```

Put `type="I"` for uppercase Roman numerals, `"i"` for lowercase roman numerals, `"A"` for uppercase letters, `"a"` for lowercase letters, or `"1"` for numbers, which is the default.

So ordered lists have a few attributes we can use: `start`, `reversed`, and `type`. Unordered lists don't have any attributes that are part of the current specification. If you want to display them differently, you need to use CSS.

So what about list items? They do have one useful attribute: `value`, which works only in an ordered list. It specifies the value of a specific list item, after which the list will continue being numbered automatically. This is useful in the event of a tie, for example.

```html
<h1>Films with most Academy Awards</h1>
<ol>
  <li>Ben-Hur (tie)</li>
  <li value="1">Titanic (tie)</li>
  <li value="1">The Return of the King (tie)</li>
  <li value="4">West Side Story</li>
</ol>
```

And guess what? You can nest lists inside one another! Aww, shucks! Just include another list inside one of the list items, before the closing tag.

```html
<h1>Roger Ebert's Grease review</h1>
<ol type="I">
  <li>Introduction</li>
  <li>Cast
    <ul>
      <li>Olivia Newton-John</li>
      <li>John Travolta</li>
    </ul>
  </li>
  <li>Plot summary</li>
  <li>Strengths</li>
  <li>Weaknesses</li>
  <li>Conclusion</li>
</ol>
```

Here I've nested a unordered list inside an ordered list. You can do that, and vice versa. Naturally, you can also nest a list inside another list of the same type.

You can, in fact, put almost any other type of element inside list items: paragraphs, headings, divs... whatever! And of course you can put inline elements in there.

```html
<h1>Roger Ebert's Grease review</h1>
<ol type="I">
  <li>Introduction
    <p><cite>Grease</cite> is worth seeing for nostaligia, but it's just an average musical.</p>
  </li>
  <li>Cast</li>
  <li>Plot summary</li>
  <li>Strengths</li>
  <li>Weaknesses</li>
  <li>Conclusion</li>
</ol>
```

So, are you ready to add a little flavor to your web pages with lists? Yeah, you are, you old list-maker, you! Until next time, I'm Davey Strus. Haaaappy hacking!
