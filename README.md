# ArduinoLatexListing
A project to enable Arduino IDE syntax highlighting in LaTeX
  
Place arduinoLanguage.tex file in your working directory (next to the latex file you're working on).  
To add it to your project, place:
```TeX
\input{arduinoLanguage.tex}  
```
somewhere before ```\begin{document}``` in your latex file.  

In your document, place your arduino code between:
``` TeX
\begin{lstlisting}[language=Arduino]  
    %% arduino code here %%  
\end{lstlisting}
``` 
  
  
Or create your own style to make changes like adding non-built-in functions and variables.  After ```\input{arduinoLanguage.tex}```, but before ```\begin{document}```, place:
``` TeX
  \lstdefinestyle{myArduino}{  
    language=Arduino,  
    %% make listing changes here %%  
  }  
 ``` 
And in your document place your arduino code between:
``` TeX
  \begin{lstlisting}[style=myArduino]  
    %% arduino code here %%  
  \end{lstlisting}  
``` 
