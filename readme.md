Markdown Presenter
==================

This is what I use for giving simple, quick-to-produce presentations. Rather than fighting with keynote or powerpoint for hours, i can whip up a presentation in minutes using markdown.

Demo and usage
--------------
Check out a demo
[here](http://chrishulbert.github.com/MarkdownPresenter/Presenter.html).
Use the arrow keys on your keyboard to switch between slides.

You can reload the presentation at any time - staying on the same
slide number - by pressing the spacebar.

Installing
----------
You need to install this on a web server, otherwise it won't be able
to open the presentation.md file via AJAX. So, if you're on a Mac,
copy it to your ~/Sites/MyPresentation folder. Then open your web
browser to http://localhost/~myusername/MyPresentation/Presenter.html.

On Linux or Mac you have also likely Python installed and can start
its built-in web server in this directory by running `python -m SimpleHTTPServer`.

Markdown file
-------------
The presentation.md file is where you put your presentation. All you need to do to separate slides is a paragraph with an exclamation mark, eg:

    This is a slide
    Blah blah blah

    !

    This is another slide
    Yada yada yada

How it works
------------
The `Presenter.html` fetches the `presentation.md` from the server via
Ajax, uses [Showdown.js](https://github.com/coreyti/showdown) to
transform it into HTML, splits it on `<p>!</p>` into individual
slides, and displays the current slide.
