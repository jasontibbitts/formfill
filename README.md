# formfill
A simple tool to fill form fields in an opendocument file.

## What does it do?
Not much.  You give it an opendocument file and a list of field/value pairs, it
looks through the document's contents for matching fields and replaces their
values with the ones you supply.  Then it can either print the result, give you
a PDF or a new opendocument file.

It will also dump out the xml for the various fields if you ask nicely.

## Why?
Well, you could export your form to PDF and then use pdftk to fill in the
fields.  You could probably do more with pdftk than this simple tool will do,
but then you'd have to have pdftk.  Which, on a modern distro without gcj, can
be pretty difficult.  And fltk depends on itext, which isn't free, so that's
another speed bump.

And even if you have pdftk, you still have to format the values and such.
formfill lets you put that stuff on the command line.

## What doesn't it do?
Well, currently it doesn't manipulate any kind of field beyond a text field.
And you can probably kill it somehow.  It doesn't handle spaces or equals signs
in field names.
