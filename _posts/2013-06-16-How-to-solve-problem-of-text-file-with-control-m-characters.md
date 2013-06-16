---
layout: post
category : Trick
tags : [control m,dos2unix]
---

{% include JB/setup %}


In linux system when viewing text files which were edited 
in windows, we may suffer troubles by strange characters, and ^M is an usual one.

<img src ="/assets/images/controlm.jpg" />

The ^M problem is caused by the difference of line terminator sysbol between windows and linux. The ^M characters are carriage returns. Windows and DOS terminate lines of text with CR (^M(\r), or ASCII code 13) followed by LF (^J(\n), or linefeed, ASCII code 10). Linux uses just LF.


We could solve this by two ways. One is use a utility named dos2unix to convert file from windows style to linux style, the other one is to open text file with vim editor, and execute command line `%s/^M//g`, which will delete all ^M character. Notice that ^M is typed by pressing Control key + V+ M.
