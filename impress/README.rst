landslide-impress
=================

An impress.js theme for Landslide.

This is a somewhat pointless project, wich works, but has been 
superseded by `Hovercraft! <https://github.com/regebro/hovercraft>`_

The problem
-----------

There are myriads of presentation softwares you can use to make presentations
in. But if you are a coder, you appreciate structured text formats such as
ReStructuredText, Markdown, etc. They are readable without softwares, you can
use your favourite editor to write them, and moving text around between
slides in a presentation is easy. You probably also like open source, so you
can fix and modify the software yourself.

One of the solutions there is Landslide,
http://adamzap.com/random/landslide.html. It will generate a nice slideshow
from your text, and it has a presenter console, something that most of these
software's miss.

But then came Prezi, http://prezi.com, and turned presentation on it's head.
No longer do presentation need to emulate the old plastic overhead slides we
used in the 90's. Presentations now should slide, zoom, connect and surprise.
They need to be *coooool*.

It didn't take long for open source to come up with an answer, and produce
impress.js, http://bartaz.github.com/impress.js. It does all that Prezie
does, and a bit more. And although it doesn't have a presenter console, with
its event-API, I was able to write one, impress-console,
https://github.com/regebro/impress-console. But impress.js is an HTML tool,
you write your presentations in pure HTML, and you need to type in the
positions for each slide, in several dimensions. This is not convenient, and
as a result several attempts of making a nice GUI for impress.js is being
worked on.

But, you are a coder. And you like code, so you don't want a GUI.

The solution
------------

The solution is to write your slides in Markdown or ReStructuredText, and use
this landslide-impress theme to generate an impress.js presentation from your
text markup! This way, you get the best of both worlds. You can make your
presentation in your structured text code, in your favourite editor, and
still get an impress.js presentation out of it.

But what about layout?
----------------------

The point of impress.js is that you have control over how the slides are
positioned. With Landslide, there is no such control. What comes out is just
a linear stretch of slides, making the impress.js part pointless.

I looked into various solution to solve that, and the end-result was
that I gave up on Landslide, and built my own solution. It's called
`Hovercraft <https://github.com/regebro/hovercraft>`_. You might want
to look at it instead.

How to use
----------

This is a basic template, with no stylings at all except those you more or
less need to get a functioning presentation. You probably want to add styles,
which you can do by adding user styles to Landslide, or by modifying
screen.css and print.css that comes with the theme. This last way is easiest to do
if you fork this theme on github.

You also might want to add custom fonts. That does require you to modify this theme.

If you prepare the presentation for upload to a website, you want to use the
--copy-theme and --relative paramaters to landslide. When you do that, you
also need to make sure that the impressConsole.css gets copied if you want
the presenter console to work. To do that you need to have a .cfg file for
your presentation and use that as a parameter to landslide.

::

   [landslide]
   theme = /path/to/landslide-impress/
   source = YourPresentation.rst
   css = /path/to/landslide-impress/css/impressConsole.css
   relative = True
   copy-theme = True


Authors
-------

The landslide-impress template is written by Lennart Regebro,
regebro@gmail.com. 

It has been informed by Azu's landslide theme at
https://github.com/azu/landslide-theme, but doesn't use it's code.

License
-------

This code is licensed under the MIT license, see LICENSE.txt.
