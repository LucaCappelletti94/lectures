# lecture-notes
A LaTeX documentclass for lecture notes.

## Features

### Silenced useless warnings
Using the package [`silence`](https://ctan.org/pkg/silence?lang=en) the library silences the following warnings:

- latex
    -  You have requested package
    -  There were undefined references
    -  Command
- latexfont
    -  Size substitutions with differences
    -  Font shape
- biblatex 
    -  Using fall-back BibTeX(8)
    -  Please (re)run BibTeX on the file(s)
-  auxhook
    - Cannot patch  
- glossaries 
    - No \printglossary or \printglossaries found.

### Float related gimmicks

### Table related gimmicks
#### L
A new column type is given `L`, that allows for automatic mathmode in column.

TODO: Add usage example!

### Theorems related gimmicks
All theorems are in `definition` style, meaning that they are not in *italic*.

### Lists related gimmicks
- Lists are built to be more compact and leave less blank space.
- Using the environment `todolist` it is possible to create checklists.

TODO: Add todolist example.

### Additional gimmicks
- When a page is empty, Latex won't generate page number or other page elements.
- When you want to leave a blank line you can just leave a blank line, without adding `\\`.
- If you'd like to use roman numerals there a command for that: `\rom{your number goes here}`.