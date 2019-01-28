# lectures
A LaTeX documentclass for lecture notes.

## Usage
### Including the document class
You can include the document class `lectures` as follows:

```latex
\documentclass{lectures}
```

To specify a particular language (currently supported just *italian* and *english*) you can do the following:

```latex
\documentclass[italian]{lectures}
```

### Title page
One of the main features of the library is the provided title page. You can create it as follows:
```latex
\documentclass{lectures}
\begin{document}
    \maketitle{
      Your title
    }{
      First author name,Second author name
    }{
      First professor name,Second professor name
    }{
      Parlo Parloni,Parletti Parini
    }{
      Year
    }{
      CFU of the course
    }{
      Informatica
    }{
      University name
    }{
      Country
    }

\end{document}
```

## Features

### Silenced useless warnings
Using the package [`silence`](https://ctan.org/pkg/silence?lang=en) the library silences the following warnings:

- **latex**
    -  You have requested package
    -  There were undefined references
    -  Command
- **latexfont**
    -  Size substitutions with differences
    -  Font shape
- **biblatex** 
    -  Using fall-back BibTeX(8)
    -  Please (re)run BibTeX on the file(s)
-  **auxhook**
    - Cannot patch  
- **glossaries** 
    - No \printglossary or \printglossaries found.

### Float related gimmicks
All floating objects are automatically centered and set to `H` as position with other objects.

### Table related gimmicks
#### L
A new column type is given `L`, that allows for automatic mathmode in column.

TODO: Add usage example!

### Theorems related gimmicks
All theorems are in `definition` style, meaning that they are not in *italic*.

Proofs are treated as theorem environments.

The following theorem-like environments are provided: 
- theorem
- corollary
- lemma
- proposition
- observation
- definition
- complexity
- property
- problem
- proof

### Lists related gimmicks
- Lists are built to be more compact and leave less blank space.
- Using the environment `todolist` it is possible to create checklists.

TODO: Add todolist example.

### Additional gimmicks
- When a page is empty, Latex won't generate page number or other page elements.
- When you want to leave a blank line you can just leave a blank line, without adding `\\`.
- If you'd like to use roman numerals there a command for that: `\rom{your number goes here}`.