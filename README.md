BashPodder was written by Linc Fessenden with the generous code contributions and great ideas of many of its users, some of whom have contributed modified scripts of their own. Version 2 is an unofficial fork by Ben Cotton that will be sent upstream when finished. BashPodder is currently licensed under the GPL. BashPodder was written to be small and fast, and most importantly, to conform to the KISS rule (Keep It Simple Stupid). That way, anyone can add to and detract from the script to suit their own needs (and they are welcome to do so). BashPodder is listed in many places as a "Linux" podcatching client, and in fact, that is what I wrote it for initially, however, it should be noted that I have dozens of emails telling me how well it works on everything else, including but not limited to MaxOSX, Solaris, AIX, Net Open and FreeBSD, even windows and many other OS's I have forgotten I am sure.

Bashpodder requires you have bash (but I have heard it runs fine under korn as well), wget or curl, sed and xsltproc.

## Todo
* bashpodder is feature complete (for now)

## Known bugs
* The sed fallback if xsltproc fails also grabs images, etc. I could require a specific file extension (e.g. mp3, wma, whatever), but that seems like a maintenance nightmare. The short term solution is "have a good XSL file". The script will put one in place for you if you don't supply one.
