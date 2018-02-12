BashPodder was written by Linc Fessenden with the generous code contributions and great ideas of many of its users, some of whom have contributed modified scripts of their own. podbasher 2 is "soft" fork (or a spork?) by Ben Cotton that adds some complexity while keeping the general ethos of BashPodder. podbasher licensed under the GPLv3.

Bashpodder requires you have bash (but I have heard it runs fine under korn as well), wget or curl, sed and xsltproc.

## Todo
* bashpodder is feature complete (for now)

## Known bugs
* The sed fallback if xsltproc fails also grabs images, etc. I could require a specific file extension (e.g. mp3, wma, whatever), but that seems like a maintenance nightmare. The short term solution is "have a good XSL file". The script will put one in place for you if you don't supply one.
