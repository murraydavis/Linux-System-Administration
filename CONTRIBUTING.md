### Guidelines for Contributors

This document provides guidelines for suggesting changes to this Linux System Administration project. The suggestions are few and fairly simple. Feel free to propose any changes to this document.

### LaTeX

This book is generated using the LaTeX document preparation system. I would be very pleased to receive recommendations on how to improve the quality of the final product, the PDF document called main.pdf. Thus, I would happily countenance suggestions that would improve the quality of the typesetting and general appearance.

If you wish to supply actual code examples in the LaTeX format, I ask that you use the same LaTeX format for the command prompt that I use throughout the document...as well as the pound symbol for comment lines.

&#35;<br>
&#35; An example of a bash command...print the current working directory.<br>
&#35;<br>
&#191;\tld&#191; pwd<br>

The best way to typeset a command prompt that appears as a tilde [~] centered inside square brackets is to use my **tld** LateX macro: 
```
\newcommand{\tld}{[\raisebox{0.5ex}\texttildelow{}]}<br>
```

The upside down question marks is a feature of the lstlisting package. At the start of each code section, I define typesetting properties. If bash command output is not in tabular form...<br>
```
\begin{lstlisting}[escapeinside={¿}{¿},frame=single,breaklines]
```
If bash command output is in tabular form...<br>
```
\begin{lstlisting}[escapeinside={¿}{¿},frame=single,breaklines,columns=fixed]
```
### Linux Code

Linux code should conform to standard bash syntax. Please test your code to ensure that it works and provide the output of commands. If you use .bashrc aliases and functions as part of your command, please provide those aliases and functions.

### References

Please provide appropriate URL links to original sources so that we can uphold the tradition of properly attributing ideas to their author.

### How you can contribute

* By following the Code of Conduct, see Code_of_Conduct.md.

* Read the entire book first. You may have a good idea and want to contribute something important. However, it is possible that I have covered your area of interest in a later section of the book. Perform a cursory search for your topic or for a keyword.

* Finding spelling errors and identifying poor grammar usage. I hold the old-school belief that spelling mistakes and poor implementation of the rules of grammar impede the flow of ideas and distract the reader. I am not holding myself out as a paragon of good writing, but I do strive with a perfectionist edge towards the goal of writing intelligently and correctly.

* Finding syntax errors in coding blocks. Spelling errors in the code blocks would be fatal to command execution. I may have also entered a command in a command table that is not correct and that does not work. 

* I have included a todo list at the back of the book. Any help completing this list would be appreciated. Actually, this is not a great place for a todo list. I will eventually move it to a 'Task List' in the github repository.

#### How to submit or make a contribution

The best way is to suggest something or make a solution is via [Github Issues for my project](https://github.com/murraydavis/Linux-System-Administration/issues). Please read the [Github Issues Guide](https://guides.github.com/features/issues/) for help on how to do this.

Please do not contact me via email with suggestions. I will monitor my email address, but not on a daily basis. I would like to use it solely for responding to contraventions of the Code of Conduct. I work full time so I will not have time to respond to trivial or insulting each emails. Full-time work is my main endeavour and the source of my home-made bread and inexpensive margarine.







