## Linux System Administration My 90:9:1 Contribution

### A Latex Compiled Document on Mastering the Command Line for Linux System Administration

The documents in this GitHub repository will allow you to compile a LaTeX package of documents in order to generate a PDF book called main.pdf. If you don't want to compile the documents, you can instead just get the book, the main.pdf document. The book is about 340 pages long and includes a table of contents, a list of figures and tables, and an index of keywords, all of which are dynamic links.

#### Github Site and downloading main.pdf

When you click on main.pdf document from within the github site, the document is rendered as html within your web browser, but not as a true pdf document with dynamic links. Apparently that feature is coming soon to the github website. As well, if you right-click main.pdf and choose to save it locally to your PC, it does not download correctly as a pdf document. The easiest way to get the main.pdf document is just to download the whole repository. Click on the green button "Clone or download". Download the zip file, go to the download folder, unzip the zip file, cd into the unzipped folder, and then launch main.pdf with firefox. Those familiar with github can of course simply clone the repository using either SSH or HTTPS.

```
unzip Linux-System-Administration-master.zip
cd Linux-System-Administration-master/
firefox main.pdf &
```

#### Sourceforge Site and downloading main.pdf

I also cloned this project to Sourceforge. It is available at: [Linux-System-Administration](https://sourceforge.net/projects/linux-system-administration). Fortunately, if you just want main.pdf, you can right-click on the file and open it with your default Adobe reader or save it locally.

### Content

This book is based on Fedora 22/23. It covers the following topics:

1. Creating user profiles in order to define command prompts, aliases, and functions

2. Bash programming

3. Linux builtin commands and GNU CoreUtils

4. manpages

5. vi text editor

6. find command and simple file tricks

7. text processing and Regex: grep, awk, sed

8. Managing users and groups: useradd, userdel, usermod, groupadd, groupdel, groupmod

9. Monitoring and managing processes: ps, strace, pgrep, nice, renice 

10. Archive and compression tools: zip, tar, gzip, zgrep

11. dnf package manager

12. SELinux

13. Network processes

14. ACLs, setuid, setguid, sticky-bit


### Compile Steps using TeXstudio

1. Complile main.tex. Click the green compile arrow or press F6.

2. Create a user command. Click Options/Configure Texstudio and then choose the build menu on the left-hand side. Name the user command: Make Nomenclature. The command is: makeindex -t %.nlg -o %.nls %.nlo.

3. Run the user command. Click Tools/User1. Make Nomenclature or press Alt-Shift-F1.

4. Compile main.tex a second time.

5. Open main.pdf from within TeXstudio. Click the page icon with the magnifying glass. main.pdf should open inline on the right-hand side. Click the red PDF icon as the top of the inline PDF to open in your external PDF viewer.

### Notes about directory structure and main.tex.

main.tex is located in the root directory and when compiled it creates main.pdf. It calls three packages that help define typesetting rules.

* settings/macros.tex

* settings/packages.tex

* settings/page.tex

main.tex also calls 19 other .tex documents in order to build the structure of the document.

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
