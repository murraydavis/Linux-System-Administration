## Writing about Linux System Administration using LaTeX

### Revisions

I began an update on March 20, 2021 working on a Fedora 33 build. See:
REVISION.MAR20.2021.md for the revisions needed to get main.tex to compile
correctly.

### A Latex Compiled Document on Linux System Administration using the command line

This article is principally about one thing: working at the command line using Linux builtin commands and [Gnu Coreutils](http://www.gnu.org/software/coreutils/coreutils.html). If you become proficient at the command line, you will have mastered an important piece of becoming a Linux System Administrator. I wrote this book using the LaTeX typesetting system, thus the title of this article is: Writing about Linux System Administration using LaTeX.

My intention was to create a high-quality typeset book that covers many topics that will appeal to those new to Linux and new to the command line. As well, the book should also be helpful to junior Linux System Administrators wishing to improve their understanding of scripting and working at the command line.

### Content of the book

This book was written on Fedora 23/24/25. However, most commands should work on Debian based systems such as Ubuntu. The biggest difference will be that Debian based systems use apt as a package manager whereas Fedora uses dnf. The book has the following chapters:

#### Chapter 1. Is ya 'ard at it al de time or wa?

This is a an attempt to provide context as to why I chose to write about the Linux command line.

#### Chapter 2. An Important Chapter

My intention was to get the reader's attention. I cover the basics of how to compile a LaTeX project and some of the challenges of typesetting code. As well, I begin to explore the topics that frustrate new users to world of Linux. For example, I write about the use of quotations, backticks, parenthesis, spaces in file names, file name expansion, regex, grep, command substitution, and variable evaluation when using single and double quotations.

#### Chapter 3. Programming

This chapter follows on the previous chapter discussing such topics as: exit codes, redirecting stdout and errors, test constructs, here string and here documents, IFS, EOF, calling functions, variable names and shell levels, as well as continuing the discussion on the use of different parenthesis.

#### Chapter 4. Manual Labour

This is an rather deep exploration of how to use manpages as an aid to understanding the command line. As an illustration of some of the concepts covered in the previous chapter, I write about how to extract specific information from manpages instead of simply calling the full manpage. Alternatives to the manpage are explored: --help, emacs, info, and coreutils. As well, I discuss how to view manpages as html, creating PDF documents from the manpages and printing manpages.

#### Chapter 5. Vi Text Editor

I discuss the difference between vim-minimal and vim-enhanced. I explore vi's three modes: vi, insert, and ex. I also cover moving, deleting, substituting, and searching for text.  I then cover working with columns, windows, indenting, marking, and creating a custom .vimrc file.

#### Chapter 6. Finding files

This chapter explores many of the daily task that a system administrator faces when searching for documents containing specific text. Regex, grep, awk, and sed are covered.

#### Chapter 7. setuid, setguid, and sticky-bit

I provide a brief overview of these topics and how to set and modify these features.

#### Chapter 8. Access Control List - ACL

I discuss the getfacl and setfacl commands and provide many examples.

#### Chapter 9. Simple file tricks

This explores in more depth the topics introduced in Chapter 6. The use of for loops and test commands are covered. I provide illustrations of how to delete and insert lines and remove duplicate lines.

#### Chapter 10. Users and groups

The topics covered include creating, deleting, modifying, and disabling users as well as groups. I provide illustrations of these commands: useradd, userdel, usermod, passwd, chage, groupadd, groupdel, and groupmod.

#### Chapter 11 processes

This is the longest chapter in the book. I cover the ps, pgrep, kill, killall, and pkill commands. I also cover the topic of modifying the priority of processes using the nice and renice commands. I also cover the top, htop, and atop monitoring tools.

#### Chapter 12 dnf

dnf is the package manager for Fedora, CentOS, and Redhat.


#### Chapter 13. The Big Squeeze

Archive and compression tools: zip, tar, gzip, zgrep.

#### Chapter 14. Network processes

A brief introduction to TCP and UDP.

#### Chapter 15. SELinux

The SELinux package is introduced.

### How to get the PDF book without compiling

Since the book is in PDF form and shared as a [github project](https://github.com/murraydavis/Linux-System-Administration), this article provides a summary of what you get when you clone my github project or when you simply download the book itself.

The source documents in the GitHub repository will allow you to compile the LaTeX documents in order to generate the PDF book called main.pdf. If you don't want to compile the documents, you can instead just get the book, the main.pdf document. The book is about 340 pages long and includes a table of contents, a list of figures and tables, and an index of keywords; all of which are dynamic internal links within the PDF book.

#### Github Site and downloading main.pdf

When you click on main.pdf document from within the github site, the document is rendered as html within your web browser, but not as a true pdf document with dynamic links. Apparently that feature is coming soon to the github website. As well, if you right-click main.pdf and choose to save it locally to your PC, it does not download correctly as a pdf document. The easiest way to get the main.pdf document is just to download the whole repository. Click on the green button "Clone or download". Download the zip file, go to your download folder, unzip the zip file, cd into the unzipped folder, and then launch main.pdf with firefox. Those familiar with github can of course simply clone the repository using either HTTPS...covered a bit later in this document. Here is how to extract and launch main.pdf from the command line.

```
unzip Linux-System-Administration-master.zip
cd Linux-System-Administration-master/
firefox main.pdf &
```

#### Sourceforge Site and downloading main.pdf

I also cloned this project to Sourceforge. It is available at: [Linux-System-Administration](https://sourceforge.net/projects/linux-system-administration). Fortunately, if you just want main.pdf, you can right-click on the file and open it with your default Adobe reader or save it locally.

### Compiling the source code


The following steps are for those who wish to clone my project files and compile main.tex to produce main.pdf.

1. First clone the project to your PC. You typically will do this using the web command provided by github...the green Cone or Download button.

```
cd yourdirectory
git clone https://github.com/murraydavis/Linux-System-Administration.git
```
The above assumes that you have the git package installed. The command downloads all the source files into a directory called: Linux-System-Administration. If you cd into this directory and issue the list command, you will see the following:

```
ls -l
rw-r--r--. 1 you yourgroup    3226 Dec  1 18:49 CODE_OF_CONDUCT.md
drwxr-xr-x. 2 you yourgroup    4096 Dec  1 18:49 content
-rw-r--r--. 1 you yourgroup    4303 Dec  1 18:49 CONTRIBUTING.md
drwxr-xr-x. 2 you yourgroup    4096 Dec  1 18:49 figures
-rw-r--r--. 1 you yourgroup   35129 Dec  1 18:49 GNU_General_Public_License.lic
drwxr-xr-x. 2 you yourgroup    4096 Dec  1 18:49 langdefs
drwxr-xr-x. 2 you yourgroup    4096 Dec  1 18:49 literature
-rw-r--r--. 1 you yourgroup 3281413 Dec  1 18:49 main.pdf
-rw-r--r--. 1 you yourgroup    3382 Dec  1 18:49 main.tex
-rw-r--r--. 1 you yourgroup    4378 Dec  1 18:49 README.md
drwxr-xr-x. 2 you yourgroup    4096 Dec  1 18:49 settings
```

This download preserved the document structure. You can now compile main.tex. I uploaded main.pdf to the github project so users could simple get that document without having to compile the source code.

#### Compile at the command line.

You will want to compile twice in order to get the index.

```
pdflatex main
pdflatex main
```
You will now have the following additional documents: main.aux, main.idx, main.lof, main.log, main.lot, main.out, main.tdo, main.toc. The compiled document, main.pdf gets overwritten.

#### Compile using TeXstudio

1. Open the main.tex file.

2. Create a user command that is required to create the index at the end of
   main.pdf. Click Options/Customize TeXStudio/Build and then
   click the Add button. Call the user command: user0:Make Nomenclature. The
comand is: makeindex %.nlo -t %.nlg -o %.nls. Run the command: Tools/Users and
chose 1. Make Nomenclature or press Alt-Shift-F1.

3. Click the compile icon or press F6. Repeat this process so that the index is
   created.

4. Open main.pdf from within TeXstudio. Click the page icon with the magnifying glass. main.pdf should open inline on the right-hand side. Click the red PDF icon as the top of the inline PDF to open in your external PDF viewer.

#### Notes about directory structure and main.tex.

main.tex is located in the root directory and when compiled it creates main.pdf. It calls three packages that help define typesetting rules.

* settings/macros.tex

* settings/packages.tex

* settings/page.tex

main.tex also calls 20 other .tex documents in order to build the structure of the document.

* content/title_page_1

* content/ch_intro

* content/ch_handy

* content/ch_program

* content/ch_manuals

* content/ch_profiles

* content/ch_vi

* content/ch_find

* content/ch_setuid

* content/ch_acl

* content/ch_file_tricks

* content/ch_users_groups

* content/ch_processes

* content/ch_dnuf

* content/ch_compression

* content/ch_network

* content/ch_selinux

* content/ch_kernelservices

* content/ch_workingwithdrives

* content/ch_solutions

These documents in turn may call images (*.png files) from the __figures__ directory. The __notes__ directory is just for notes and not part of the compile process. I played around with embedding videos in the LaTeX document but bailed after many failed attempts. The __settings__ directory also contains _url.tex_ and _urlindex.tex_. I played around with creating an index of all urls, but put off implementing that feature since it is quite complex and breaks other formatting.
