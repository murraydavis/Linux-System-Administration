## Compile of main.tex did not work...on a Fedora 33 system.

### My system
$ tex --version
TeX 3.14159265 (TeX Live 2020)
kpathsea version 6.3.2

$ uname -r
5.10.23-200.fc33.x86_64

### settings/packages.tex

I had to add a user package to deal with errors in ch_handy.tex,
ch_manuals.tex, ch_selinux.tex.

Remove Package inputenc Error: Invalid UTF-8 byte sequence in ch_handy.tex,
ch_manuals.tex, ch_selinux.tex
\usepackage [latin1]{inputenc}

The makeindex user command did not work in TeXStudio. I was using makeidx when
I should have been using imakeidx. I had changed the following line 135:
\usepackage{makeidx}
to: \usepackage{imakeidx}.
The solution is thanks to Ljon in my latexforum.org post: makeindex not
working, compile fine. [Latex Forum]
(https://latex.org/forum/viewtopic.php?f=51&t=34113&p=114747#p114747).

### TeXStudio
I also changed the user command in Options/Configure TeXStudio/Build.
Command name: user0:Make Nomenclature
Command: makeindex %.nlo -t %.nlg -o %.nls 

### content/ch_handy.tex
line 1121, I had to remove this line
like  --format, but interpret backslash escapes, and do not out‐

### content/ch_manuals.tex
line 458, I had to remove these lines
These  functions  return  information  about  a file, in the buffer pointed to
by stat.  No permissions are required on the file itself, but—in the case of
stat(), fstatat(), and lstat()—execute (search)  permission is required on all
of the directories in pathname that lead to the file.
