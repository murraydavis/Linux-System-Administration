### Linux System Administrator My 90:9:1 Contribution

Mastering The Command Line - A Latex Compiled Document

The documents in this GitHub repository will allow you to compile a LaTeX package of documents in order to generate a PDF document called main.pdf. However, if you are not interested in LaTeX, you cannot simply download and read the main.pdf document. github renders the main.pdf as html so it does not load as a dynamic pdf within github. As well, it does not download correctly. You can download the whole repository. Click on the green button "Clone or download". Download the zip file, go to the download, unzip the file, and then launch it with firefox.

```
unzip Linux-System-Administration-master.zip
cd Linux-System-Administration-master/
firefox main.zip &
```

### Compile Steps using TeXstudio

1. Complile main.tex. Click the green compile arrow or press F6.

2. Create a user command. Click Options/Configure Texstudio and then choose the build menu on the left-hand side. Name the user command: Make Nomenclature. The command is: makeindex -t %.nlg -o %.nls %.nlo.

3. Run the user command. Click Tools/User1. Make Nomenclature or press Alt-Shift-F1.

4. Compile main.tex a second time.

5. Open main.pdf from within TeXstudio. Click the page icon with the magnifying glass. main.pdf should open inline on the right-hand side. Click the red PDF icon as the top of the inline PDF to open in your external PDF viewer.

### Notes about directory structure and main.tex.

main.tex is located in the root directory and when compiled, it calls three packages.

* settings/macros.tex

* settings/packages.tex

* settings/page.tex

main.tex also calls 19 other .tex documents.

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
