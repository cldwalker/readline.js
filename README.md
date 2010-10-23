Description
===========
jQuery plugin which adds basic readline functionality to any html element. Goal is to mimic
essential readline behavior from the [original](http://cnswww.cns.cwru.edu/php/chet/readline/rltop.html).
Uses jquery UI 1.8.5 autocomplete widget and the hotkeys.js plugin for keybindings.

Setup
=====

Add javascript tags:

    <script src='http://ajax.googleapis.com/ajax/libs/jquery/1.4.3/jquery.min.js' type='text/javascript'></script>
    <script src='jquery.hotkeys.js' type='text/javascript'></script>
    <script src="jquery.ui.autocomplete.min.js" type='text/javascript'></script>
    <script src='jquery.readline.js' type='text/javascript'></script>

Assuming you have an html element with id #input:

    <script type='text/javascript'>
      $(document).ready( function(){ $('#input').readline() });
    </script>

For options to pass to $.fn.readline(), see documentation in the source.

Once an element is readline-enabled, it needs to have some event (i.e. submit) that adds
to the history with $.readline.addHistory(). See demo.html for an example.


Keybindings
===========
* previous line: control-p, up arrow
* next line: control-n, down arrow
* clear line: control-u
* start search history: control-r
* stop search history: control-g
* custom autocompletion: tab

Demo
====
For a simple demo, simply open demo.html in a browser and enter a few lines.
For a more advanced example, see jrepl.

Todo
====
* Fix history not saving element's current text
* Forward/backward word keybindings
* Fix exiting search history on an active menu item
* Display tab completion in multiple columns
* Deal with autocompletion dependence on images
