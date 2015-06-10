# google-style-guide-javascript-eclipse

Eclipse JavaScript Code Formatter profile based on [Google's Style
Guide](http://google-styleguide.googlecode.com/svn/trunk/javascriptguide.xml).

This was created by first importing [Google's C++
profile](http://google-styleguide.googlecode.com/svn/trunk/eclipse-cpp-google-style.xml)
and applying minor fixes to bring it closer to their JavaScript guide (some of
the C++ settings weren't correctly imported).

## ABANDONED!

I appreciate the role Eclipse played in the history of open-source development, but I no
longer use it and I can't ever see myself returning. This project never perfectly mapped
Google's style to Eclipse rules, and I haven't worked on this for 3 years.


## Installation

1. open Eclipse IDE
2. open the Preferences window
3. drill down: JavaScript -> Code Style -> Formatter
4. click Import and select the provided XML file
5. done!

## Known Issues

### Wrapping Binary and Ternary Operators

Google's JavaScript Style Guide states that when wrapping long lines
with binary (e.g. +) and ternary operations (e.g. ? :), "Always put the
operator on the preceding line, so that you don't have to think about
implicit semi-colon insertion issues. Otherwise, line breaks and
indentation follow the same rules as in other Google style guides."

#### Good

    blah ?
        blah :
        blah;

#### Bad

    blah
        ? blah
        : blah;

There doesn't seem to be an Eclipse setting to enforce this, so it is
probably good practice to try and keep these lines short if you don't
want Eclipse to break the rules.

