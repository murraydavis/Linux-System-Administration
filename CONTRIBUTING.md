### Guidelines for Contributors

This document provides guidelines for suggesting changes to this Linux System Administration project. The rules are few and fairly simple.

### LaTeX

This book is generated using the LaTeX document preparation system. I would be very pleased to receive recommendations on how to improve the quality of the final product, the PDF document called main.pdf. Thus, I would happily countenance suggestions that would improve the quality of the  typesetting and general appearance.

If you wish to supply actual code examples in the LaTeX format, I ask that you use the same LaTeX format for the command prompt that I use throughout the document...as well as the pound symbol for comment lines.

&#35;<br>
&#35; An example of a bash command...print the current working directory.<br>
&#35; The best way to typeset a command prompt that appears as a tilde [~] centered inside square brackets is to use my LateX macro: \newcommand{\tld}{[\raisebox{0.5ex}\texttildelow{}]}<br>
&#35;<br> 
&#191;\tld&#191; pwd<br>
&#35; The upside down question marks is a feature of the lstlisting package. At the start of each code section, I define typesetting properties.<br>
&#35; If bash command output is not in tabular form.<br>
\begin{lstlisting}[escapeinside={¿}{¿},frame=single,breaklines]<br>
&#35; If bash command output is in tabular form.<br>
\begin{lstlisting}[escapeinside={¿}{¿},frame=single,breaklines,columns=fixed]<br>
&#35;<br>

### Linux Code

Linux code should conform to standard bash syntax.


