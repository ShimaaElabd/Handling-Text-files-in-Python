# Handling Text files in Python

## Text Files and Encodings

The Single Most Important Fact About Encodings: It does not make sense to have a string without knowing what encoding it uses and pretend 
that “plain” text is ASCII. There Ain’t No Such Thing As Plain Text

If we have a string, in memory, in a file, or in an email message, 
we have to know what encoding it is in or we cannot interpret it or display it to users correctly As if I don't know a particular string is 
encoded using UTF-8 or ASCII or ISO 8859-1 (Latin 1) or Windows 1252 (Western European),
I simply cannot display it correctly or even figure out where it ends.
There are over a hundred encodings and above code point 127.


In this notebook I've used the glob library, Check out the docs https://docs.python.org/3/library/glob.html

glob library makes opening files with similar path structure (like the folder of Roger Ebert review text files) simple.

In this notebook I've iterated through all of the files in this folder ( Roger Ebert review)
to open and read each, then extract the bits of text that I need as separate pieces of data:

- First line, which is the movie title.
- Second line, which is the review URL.
- Everything from the third line onwards, which is the review text.
