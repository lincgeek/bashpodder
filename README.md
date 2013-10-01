BashPodder was written by Linc Fessenden with the generous code contributions and great ideas of many of its users, some of whom have contributed modified scripts of their own. Version 2 is an unofficial fork by Ben Cotton that will be sent upstream when finished. BashPodder is currently licensed under the GPL. BashPodder was written to be small and fast, and most importantly, to conform to the KISS rule (Keep It Simple Stupid). That way, anyone can add to and detract from the script to suit their own needs (and they are welcome to do so). BashPodder is listed in many places as a "Linux" podcatching client, and in fact, that is what I wrote it for initially, however, it should be noted that I have dozens of emails telling me how well it works on everything else, including but not limited to MaxOSX, Solaris, AIX, Net Open and FreeBSD, even windows and many other OS's I have forgotten I am sure.

Bashpodder requires you have bash (but I have heard it runs fine under korn as well), wget or curl, sed and xsltproc.

## Todo
* Add support for multiple users
    * External config files (in testing)
    * System-wide config file so that root can change defaults for everyone?
* Add support for verbosity
    * Say what's being downloaded
    * Allow lables in config file?
* Optionally suppress m3u creation
* Probably more things that I'll thnk of later