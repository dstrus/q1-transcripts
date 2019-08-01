Hey, everyone. Welcome to Kenzie Academy. I'm Davey Strus.

We understand tags and attributes. Now let's talk about the overall structure of an HTML page. There are a few things we ought to have on every page. Now, web browsers are very tolerant of invalid markup, and they'll do the best they can to guess what you mean, but we aim to write valid markup in the first place.

The first thing we put at the top of an HTML document is something called a doctype.

```html
<!DOCTYPE html>
```

"DOCTYPE" is not an element type, but rather a **keyword** with a special meaning. But like the element types in a tag, the word "DOCTYPE" is case-insensitive. You can write it in all-caps, all lowercase, or a mix of the two. For historical reasons, all-caps is probably still slightly more common for doctypes, because it was required to be all-caps in earlier versions of the spec, and it must be in all-caps to be valid XML. We generally don't care if our HTML happens to also be valid XML, and we'll be doing other things that would be invalid XML anyway, so I wouldn't worry about it. Feel free to use lowercase or uppercase.

So what is this "doctype" business anyway? It's something of an historical artifact. It used to be accompanied by the URL for a spec that told exactly what version of the HTML standard was being implemented in the page. But all web browsers ever really did with it was to check if the page had a doctype, and if it did, the browser would draw the page in _standards mode_—that is, a mode that assumes that you actually follow the standard when writing HTML. This is as opposed to _quirks mode_, which some browsers implement in an effort to present older, non-compliant pages the way they were originally intended—pages that were written when there weren't any browsers that properly implemented web standards.

As of HTML 5, we no longer include a URL in the doctype. It's just `<!DOCTYPE html>`. All it does, really, is tell the browser that you intend to write your HTML (and CSS, when we get to that) according to spec.

After the doctype comes the **root element**: The element that every other element will be nested inside. That element? `html`.

```html
<!DOCTYPE html>
<html>
</html>
```

There's not much to the `html` element, but you can—and should—use an attribute to specify the page's primary language.

```html
<!DOCTYPE html>
<html lang="en">
</html>
```

The value comes from the two-letter language codes in the [ISO 639-1](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) standard, which you should memorize completely. Just kidding. You don't need to do that. Anyway, I've used the code for English here.

Why bother with this? Specifying the language provides clues to search engines and to the screen reading software used by folks with visual impairments. You're free to use multiple languages on a page. Just include the `lang` attribute on another element to specify that a particular section is in something other than the page's primary language.

That's pretty much all you need to know about the `html` element. _Everything_ else on the whole page goes inside that root element. The `html` element has two child elements—that is, two elements that are nested immediately inside it. Those elements are `head` and `body`.

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>My fancy web page</title>
  </head>

  <body>
    <h1>Hello there.</h1>
  </body>
</html>
```

The stuff inside the head will _not_ appear on the page. It's metadata. The body contains everything that will actually appear on the page. When you edit HTML on CodePen, you're only writing the contents of the body.

So if the head includes stuff that doesn't actually show up, what _is_ that stuff? The example here is about as simple as it gets. It has a title, which is what will show in the tab bar of your browser. And it has a `meta` element specifying the UTF-8 character encoding. That indicates what characters—what letters, numbers, and symbols—this page is allowed to contain. If you don't have a very specific reason _not_ to use UTF-8, just stick with UTF-8, and it's a good idea to include that on every HTML page you make.

There's other metadata that you can add to a page using the `meta` element, include keywords and author information. Feel free to follow the link to [learn more](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/meta) if you'd like.

Under that, we have the `title` element. You'll want this on every page as well. In most browsers, the title shows up on the tab that the page is loaded in. The title of the active tab will also be the title of the window, so if you use Mission Control to look at all your open windows, the title you'll see if you hover over a browser window is the title of the active tab. The title also has an impact on search engine placement, so be sure to use something accurate and specific. Often, the title will be something like the name of the specific page, followed by the name of the site.

There's plenty of other stuff you can put in the `head` as well. You can link to external stylesheets, add styles directly, or link to a custom icon (known as a **favicon**, which is something else that will show up in the browser tab). You can also put JavaScript in the `head`, although that's often not the best place for it, as we'll learn when we dig into JavaScript later.

For now, we can keep the head very simple, just specifying the UTF-8 character set, and a title. Everything else—all our actual _content_—belongs in the body.

That's about it for the basic structure of HTML. Until next time, I'm Davey Strus. Haaaappy hacking!
