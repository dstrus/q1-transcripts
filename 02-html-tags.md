Hey, everyone. Welcome to Kenzie Academy. I'm Davey Strus.

HTML: Your friend and mine. We've seen it before, but we could use a slightly deeper understanding.

What is HTML? A programming language? No, not a programming language—a **markup** language. Hypertext Markup Language. Markup, because we use **tags** to _mark up_ the content of a document. This is a heading, that's a paragraph, and so on. HTML tells the web browser about your document's _structure_.

So what's that we mark it up with again? **Tags**! Wrap a piece of content in tags—an opening tag and a closing tag—and you have an HTML **element**. How do you tell an opening tag from a closing tag? Closing tags begin with a forward slash.

```html
<h1>My groovy page</h1>
```

The `h1` inside those tags tells us what type of element this is, and the tag is case-insensitive, meaning that uppercase and lowercase are treated exactly the same.

For example, `header` could be written all lowercase...

```html
<header>content</header>
```

... all uppercase...

```html
<HEADER>content</HEADER>
```

...or a mix of the two.

```html
<hEaDeR>content</HeAdEr>
```

You can do that. There's no rule against it. It is, however, considered a best practice to use all lowercase, for the sake of readability, among other things.

You'll find that we talk a lot about "best practices"—guidelines that you don't technically _have_ to follow for your code to work, but which really are a good idea. Many previous developers have suffered over the years to figure out the best approach to a lot of things, and sometimes we don't have to learn from our own mistakes. We can learn from the mistakes of others. It's what separates us from the beasts of the field!

In the mid-nineties, tags were often written in all-caps. But it turns out, all caps is just plain harder to read, because there's not as much variation in the shapes of different letters. And mixing the two would just be goofy. Have mercy on the people who have to read your markup, and stick with all lowercase. Because you know who has to read your markup? You do! When you write any given piece of code, it's unlikely to be the last time you'll ever see it. In general, your code will be read a lot more than it's written. So if you make your stuff unreadable, you're not only making things harder for your coworkers; you're making it harder on your future self.

OK, rant over.

Sometimes the opening tag will have a little something extra in it: Attributes.

```html
<a href="about.html" title="About us">About</a>
```

This `a` tag has two attributes: `href` and `title`. Each attribute has a value wrapped in quotation marks, and there's an equals sign separating each attribute from its value.

Sometimes you'll see folks leave out the quotation marks. Gross, but sometimes you can get away with it, if, for example, there are no spaces in the value. Here, we could leave the quotation marks off of the `href` value without any trouble...

```html
<a href=about.html title="About us">About</a>
```

But if we try that with the `title`...

```html
<a href=about.html title=About us>About</a>
```

...it thinks that the title is just `About`, and that `us` is a separate attribute altogether. So even though you can get away with leaving the quotation marks off sometimes, it's a best practice to always include them. And you know how I feel about best practices!

What about single-quotes vs. double-quotes?

```html
<a href='/home' title='Home page'>Home</a>
<a href="/about" title="About us">About</a>
```

You can use either one. Both are valid. Just be sure that your closing quotation mark matches the opening quotation mark. Trying to match a single-quote with a double-quote will not work. As for which one you use, however, the only difference is how you handle a quotation mark that appears in the middle of a value.

```html
<a title='It's the contact page!'>Contact</a>
```

Here, my title is surrounded by single quotes, but I use an apostrophe in the middle of the value. The browser will see that apostrophe as the closing quote, and treat `s`, `the`, `contact`, and `page!` as separate attributes, and it won't know what the heck that last single-quote is supposed to mean. You can deal with this one of two ways. You can either just use double-quotes here...

```html
<a title="It's the contact page!">Contact</a>
```

...or you can stick with your single-quotes, and use what's called an **HTML entity** for the apostrophe.

```html
<a title='It&apos;s the contact page!'>Contact</a>
```

With double-quotes, you have the same issue. If you use double-quotes around your attribute value, and the value happens to include double-quotes...

```html
<a title="The "contact" page!">Contact</a>
```

...things won't go so well. So you can either wrap it in single-quotes instead...

```html
<a title='The "contact" page!'>Contact</a>
```

...or use HTML entities inside the value.

```html
<a title="The &quot;contact&quot; page!">Contact</a>
```

Don't worry. We'll talk more about HTML entities in a later lesson. For now, it's enough to know that they give you a way to include certain special characters in your HTML.

From time to time, you'll also see **boolean attributes**. These attributes are either on or off. They're either present or they're absent.

```html
<input type="checkbox" checked>
```

This checkbox input has the boolean attribute `checked`, indicating that the checkbox should be checked when the page loads. Notice I haven't given the attribute a value at all. I could have written it with the value `checked`...

```html
<input type="checkbox" checked="checked">
```

...but with boolean attributes, the value is optional. If you want to turn it off—to leave the checkbox unchecked, in this case—you don't give the attribute a different value; you leave that attribute off altogether.

```html
<input type="checkbox">
```

So, tags and attributes: Get the picture?

Until next time, I'm Davey Strus. Haaaappy hacking!
