# note2add.sh

## Description

note2add.sh is an interactive bash script for adding, searching,
viewing, editing and deleting notes. It supports one hierarchical
level and tags. The script runs on Linux and uses native tools
that come with most distributions such as cat, grep, sed, cut,
tr. I don't know if it is POSIX compatible, it has been tested on
Ubuntu.

### How is it different from other note-taking tools?

There are other note-taking tools for the command line, but
usually you have to supply the arguments from the command line.
This script is interactive. Once you run it, it will ask you what
to do and will prompt you with some options. Thus you won't have
to remember commands and arguments.

### What file format is used?

Every note is saved in a plain text file, so you can put the
notes directory in your Dropbox or bitsync folder and it will be
synchronized.

### Quirks and limitations

I am not a programmer, so the script is a little rough around the
edges. There are some quirks, e.g. if you delete a file it will
show up in the list of files immediately afterwards, but on the
next run it won't be there. In principle, if you try to break the
script, probably you will, but if you use it reasonably, it
should work as expected.  From within the script you can edit
only the content of already existing notes. At this point you
can't change the tags and the title with which the note has been
created. If you really have to, you can do so manually, but make
sure that a) you preserve the note's syntax (regarding tags and
titles) and b) if you change the title, rename the file
accordingly.

The script defaults to "nano" as the editor for the notes.

## Installation

Just download the script 

> curl "https://raw.githubusercontent.com/egalion/note2add/master/note2add.sh" -o note2add.sh

To make it work you will have to create the notes directory
first.  For me it is "~/tn". You can change the notes directory
by opening the script with your favourite editor and editing 

> NOTES2ADD_DIR="$HOME"/tn

that can be found on line 5 of the script, e.g. to

> NOTES2ADD_DIR="$HOME"/Dropbox/tn

if you want to have the notes directory in your Dropbox folder.

Then make the script executable by doing

> chmod +x note2add.sh

and copy it to your path (e.g. "/usr/local/bin". The you will be
able to run it from your shell.

## License and Warranty

You are free to use, distribute or modify this script as you
want. It is provided without any warranty. If you use it, do so
at your own risk. I will not be responsible for any damages that
it may cause.
