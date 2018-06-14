# HTML Tidy 2 Plugin for Notepad++ utf8hack

This is basically https://github.com/bruderstein/NppTidy2 plugin with modified two lines in file  tidy-html5/src/gdoc.c in lines 144 and 145:

TY_(AddAttribute)( doc, node, "http-equiv", "Content-Type" );
TY_(AddAttribute)( doc, node, "content", "text/html; charset=UTF-8" );

which basically gives you that if you use it out of the box it will tidy up your html AND will add

<meta http-equiv="Content-Type" content="text/html; charset=utf-8" />

to your head.

The bug is that it is adding it every time you tidy so i use two diffenent configs, one with option:

tidy-mark: no

which will prevent this from happening.

Maybe someone will find it useful.


## Installation

Just copy the Tidy2.dll to your Notepad++\plugins directory.  Ideally add the doc folder to Notepad++\plugins directory too, this will mean you have the correct
documentation, and the "Show Config Help" option will show the documentation that applies to your version (rather than simply the latest on the web)
