#!/bin/bash
# By Linc 10/1/2004
# Find the latest script at http://lincgeek.org/bashpodder
# Revision 1.21 12/04/2008 - Many Contributers!
# If you use this and have made improvements or have comments
# drop me an email at linc dot fessenden at gmail dot com
# and post your changes to the forum at http://lincgeek.org/lincware
# I'd appreciate it!

# Make script crontab friendly:
cd $(dirname $0)

# datadir is the directory you want podcasts saved to:
datadir=$(date +%Y-%m-%d)

# create datadir if necessary:
mkdir -p $datadir

# Delete any temp file:
rm -f temp.log

# Read the bp.conf file and wget any url not already in the podcast.log file:
while read podcast
	do
	file=$(xsltproc parse_enclosure.xsl $podcast 2> /dev/null || wget -q $podcast -O - | tr '\r' '\n' | tr \' \" | sed -n 's/.*url="\([^"]*\)".*/\1/p')
	for url in $file
		do
		echo $url >> temp.log
		if ! grep "$url" podcast.log > /dev/null
			then
			wget -t 10 -U BashPodder -c -q -O $datadir/$(echo "$url" | awk -F'/' {'print $NF'} | awk -F'=' {'print $NF'} | awk -F'?' {'print $1'}) "$url"
		fi
		done
	done < bp.conf
# Move dynamically created log file to permanent log file:
cat podcast.log >> temp.log
sort temp.log | uniq > podcast.log
rm temp.log
# Create an m3u playlist:
ls $datadir | grep -v m3u > $datadir/podcast.m3u
