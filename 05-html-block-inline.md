Further reading:
* [Inline elements](https://developer.mozilla.org/en-US/docs/Web/HTML/Inline_elements) on MDN
* [Block-level elements](https://developer.mozilla.org/en-US/docs/Web/HTML/Block-level_elements) on MDN

Hey, everyone. Welcome to Kenzie Academy. I'm Davey Strus.

We've been happily nesting elements inside one another, and it's been fine.

As long as you get your closing tags in order, you can put elements inside one another.

```html
<p>
  I'm <em>so</em> bored!
</p>
```

When you do that, the enclosing element is said to be the **parent** of the inner element, and the inner element is said to be the **child** of the enclosing element.

Ah, but what if the child has children of its own?

```html
<body>
  <p>
    Let's read <cite>Thud!</cite>
  </p>
</body>
```

The paragraph is a child of `body`, and the citation is a child of the paragraph. So what's the relationship between `body` and `cite`? Why, `cite` is the body's **grandchild**!

Let's go deeper!

```html
<html>
  <body>
    <p>
      Let's read <cite>Thud!</cite>
    </p>
  </body>
</html>
```

Terms like great-grandparent aren't all that useful when looking at markup. At that point, we just call them **ancestors** and **descendants**. The `html` element is an ancestor of every other element on the page, and every other element is a descendant of the `html` element. We'll talk more about this and the tree-like structure it suggests much later. That's all you need to know for now.

So now we know all about nesting elements inside one another, and you can probably nest _any_ element inside any other, right? Nope! There are rules.

To determine which elements can be nested inside one another, we first need to understand the difference between **block-level** elements, and **inline** elements. HTML 5 actually reclassified HTML elements using a much more complicated system that frankly isn't terribly useful when starting out, and understanding the old classifications of block-level and inline _are_ useful, so we're going to stick with those for learning purposes.

The super-short version is that block-level elements start a new line and fill the width of their containers. Inline elements can start and end in the middle of a line.

Examples of block-level elements that you already know include `h1` through `h6` and paragraphs. Inline elements that you're familiar with include `em`, `strong`, `cite`, `i`, `b`, and `u`.

So what are the implications for which elements can be nested inside other elements? Well, as you might guess, you can't put a block-level element inside an inline element. You _can_ put one inline element inside another. And you can put a block-level element inside another block-level element... sometimes. There are some pretty big exceptions. In fact, you cannot put any block-level elements inside a paragraph or inside headings, `h1` through `h6`. That means we actually haven't talked about any elements that can contain other block-level elements yet.

Meet the `<div>`. It's short for _content division_, and it's a semantically meaningless element. It serves no purpose other than as a container for other elements. It's a block-level element, and it can contain any other element that belongs in the body. It's not terribly useful until you dig into CSS, but it's good to know that it exists for those occasions when you need some sort of container and there's no more appropriate element. It is essentially the generic block-level element.

As you might guess, there's an inline equivalent: `<span>`. It doesn't _mean_ anything. It's just a generic, inline container. But sometimes that's just what you need, because you need to apply some inline CSS, and a more appropriate semantic element doesn't exist.

And that's about all there is to it. Until next time, I'm Davey Strus. Haaaappy hacking!
