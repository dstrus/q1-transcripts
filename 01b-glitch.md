Hey, everyone. Welcome to Kenzie Academy. I'm Davey Strus.

To get started making web sites, we're going to use a web-based editor called Glitch. Glitch is a pretty impressive IDE, or Integrated Development Environment, that runs right in the web browser. You don't have to install anything to use it, and it's really quick and easy to get started.

Just visit [glitch.com](https://glitch.com/), and look for the **New Project** button. You'll see the **Sign In** button next to it, but we don't need to sign in just yet. Go ahead and click **New Project** to start a new project.

You'll be given a few choices at this point, because Glitch offers several templates for new projects, and it also lets you use a Git repository as the basis for your new project. Git is a source code management tool, and you'll learn all about it later. For now, just take my word for it that it's really cool that Glitch lets you do this. For our purposes, the **hello-webpage** template will do nicely.

You'll see a loading screen for a moment, and Glitch is kind enough to show tips on its loading screens, so you're not just sitting there doing nothing.

Pretty soon, you'll see your project. Let's go through the different sections of the interface, starting with the toolbar across the top.

First, you'll see the **Project Options** menu. It's labeled with the name that was automatically assigned to your project. Open the menu, and you'll see a variety of options. This is where you can make a new project, make a copy of this project (which Glitch calls "remixing"), and other project-related things. You can change some editor options here as well, like changing the color theme. There's also a handy reference for Glitch's keyboard shortcuts. You might want to check those out some time.

Next is the **Show** menu. This is where you can actually view the web site you've made. You can open it in a new window, or side-by-side with your editor. I'll open mine next to the code. Very cool! We'll open this up again later, but for right now, I'm going to close it by clicking the **X** at the top of the preview.

Next is a search bar where you can quickly jump to any file in your project. This is really handy when you have large projects. Even better, you can jump to this search bar any time using the keyboard shortcut Command+P.

On the right side of the toolbar, you'll see the **Sign In** button, and the **Glitch Options** menu. The **Glitch Options** menu has links to the Glitch homepage, the documentation, the forum, and more. It's definitely worth your time to check out the documentation at some point.

Next, we have the sidebar and the editor itself. At the top of the sidebar is the **Share** menu, where you'll find a number of options for sharing the project with others. You can play around with the different options. Try opening the different share links in a private browsing session or in a separate browser, like Safari or Firefox, to see how each of them works.

You'll also find a button for toggling the sidebar. You can also toggle the sidebar with Command+I on the keyboard.

Below all that is the file list. The new project was created with four files: A README, an HTML file, a JavaScript file, and a CSS file. There's also a place to drop in assets. Assets are files that contain something other than plain-text—like images or audio files. Try switching between the files in the file list. As you do that, the file you've selected loads in the editor. Remember, you can also switch files using the search bar, and you can get to the search bar quickly with Command+P. The cool thing about the search bar is that you can type any part of the file name. You don't have to start at the beginning. So I can hit Command+P, then type "html", and the list narrows down to just my HTML file. Hit _tab_ to select it, then press _return_ to switch to that file.

You can also create a new file in the sidebar. Keep in mind that you'll need to include the file name extension, like `.html`, and notice that you can even nest a new file inside a folder by including a forward slash in the file name. Try it out! You can also upload files from your computer.

At the bottom of the sidebar, you'll find two more buttons. The first is the "Rewind" button. This is how Glitch implements multiple levels of _undo_. Since you can collaborate with others on projects, it even shows who made each edit. We haven't actually made any changes to this file yet, so there's not much point in playing with that right now, but you should check it out on your own some time.

The **Tools** menu offers some more features that are beyond our needs at the moment, but you may wish to read up on them or experiment with them on your own.

That brings us to the heart of the application: The editor. This is where the magic happens. You can edit whichever file you have selected in the sidebar, and if you have the preview open, you'll see the changes happen live. Let's try that out!

Open the preview using the **Show** menu in the toolbar. Once again, I'll open it next to the code, rather than in a new window. Now try making some changes to the HTML file, and watch what happens. I see a big heading that says "Hi there!", so I'll look for where that appears in the code. There it is. I'll just change that... and the changes show up almost immediately! And Glitch saves your work automatically. You never have to manually save it. If the preview ever does appear to be out of sync with your code, just hit the **Refresh** button at the top of the preview.

Next to the **Refresh** button, you'll see a button labeled **Change URL**. By default, the preview will show the file `index.html`, regardless of what file you have open in the editor. If you want to view a different file, you can browse to a different file using the **Change URL** button.

So if I create a new file called `howdy.html` and put some text in there, I can change to that file by clicking **Change URL** and typing "howdy.html". To change back, click **Change URL** again, and click **Reset**. That sends us back to `index.html`. If you find that you're having trouble switching to a new file, double-check that you typed the name exactly right. Glitch will refuse to change URLs if you give it a file name that doesn't actually exist in your project.

Now back to the editor itself for a moment. Let's open up `index.html` again. The editor includes _syntax highlighting_, meaning that it shows things in different colors depending on context. In this theme, tags show up in blue, and attribute values show up in red. That not only makes it easier to find things; it also makes it easier to catch your mistakes. If something doesn't change colors when you expect it to, then you probably mistyped something.

I'm going to add an `h2` element underneath the paragraph on this page. Watch what happens as soon as I finish typing the opening tag. It automatically adds the closing tag, puts in some line breaks, and puts my cursor in between. It even indents it for me!

The editor does some other pretty cool things, so feel free to experiment, and don't forget to check out the documentation.

At some point, this message will have popped up:

> **Create an account** to keep this project, and edit it anywhere.

Although you can use Glitch without signing in, if you want your projects to stick around, you do need to create an account. You can sign in using a third-party service like GitHub or Google, or you can create an account using your email address. Sooner or later, you're going to want to sign in one way or another.

So that's a quick overview of Glitch. Poke around, experiment, learn on your own. Have fun!

Until next time, I'm Davey Strus. Haaaappy hacking!
