# Lectures

[![GitHub Actions](https://github.com/LucaCappelletti94/lectures/actions/workflows/latex.yml/badge.svg)](https://github.com/LucaCappelletti94/lectures/actions)
[![Version](https://img.shields.io/badge/CTAN_Version-1.0.6-blue.svg)](https://ctan.org/pkg/lectures)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](https://github.com/LucaCappelletti94/lectures/blob/main/LICENSE)
[![Available in](https://img.shields.io/badge/Available_in-TEX_Live-green.svg)](https://ctan.org/pkg/texlive)
[![Available in](https://img.shields.io/badge/Available_in-MiKTEX-green.svg)](https://ctan.org/pkg/miktex)

A LaTeX documentclass for lecture notes.

## Usage

### Including the document class

You can include the document class `lectures` as follows (the default language is *english*):

```latex
\documentclass{lectures}
```

To specify a particular language (currently supported just *italian* and *english*) you can do the following:

```latex
\documentclass[italian]{lectures}
```

or, analogously:

```latex
\documentclass[english]{lectures}
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

[![Title page example](https://github.com/LucaCappelletti94/lectures/blob/master/title_page_example.png?raw=true)](https://github.com/LucaCappelletti94/lectures/blob/master/title_page_example.png)

## Features

### Silenced useless warnings

Using the package [`silence`](https://ctan.org/pkg/silence?lang=en) the library silences the following warnings:

- `latex`:
  - You have requested package
  - There were undefined references
  - Command
- `latexfont`:
  - Size substitutions with differences
  - Font shape
- [`biblatex`](https://ctan.org/pkg/biblatex):
  - Using fall-back BibTeX(8)
  - Please (re)run BibTeX on the file(s)
- [`auxhook`](https://ctan.org/pkg/auxhook):
  - Cannot patch
- [`glossaries`](https://ctan.org/pkg/glossaries):
  - No \printglossary or \printglossaries found.

### Float related gimmicks

All floating objects are automatically centered and set to `H` as position with other objects.

### Table related gimmicks

#### L, C and R

New column types are given `L`, `C`, and `R`, that allow for automatic mathmode in columns.

Example usage:

```latex
\documentclass{lectures}
\begin{document}
\begin{tabular}{L C R}
  a & b & c \\
  \alpha & \beta & \gamma \\
  x_1 & x_2 & x_3 \\
\end{tabular}
\end{document}
```

### Theorems related gimmicks

All theorems are in `definition` style, meaning that they are not in *italic*. All environments are color-coded to facilitate reading and reviewing.

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

Example usage:

```latex
\documentclass{lectures}
\begin{document}

\begin{theorem}[Pythagorean Theorem]
In a right-angled triangle, the square of the hypotenuse is equal to the sum of the squares of the other two sides.
\begin{equation}
a^2 + b^2 = c^2
\end{equation}
\end{theorem}

\begin{proof}
This can be proven using the properties of similar triangles.
\end{proof}

\begin{definition}[Prime Number]
A prime number is a natural number greater than 1 that has no positive divisors other than 1 and itself.
\end{definition}

\end{document}
```

[![Theorem example](https://github.com/LucaCappelletti94/lectures/blob/master/example.png?raw=true)](https://github.com/LucaCappelletti94/lectures/blob/master/example.png)

### Lists related gimmicks

- Lists are built to be more compact and leave less blank space.
- Using the environment `todolist` it is possible to create checklists.

Example usage:

```latex
\documentclass{lectures}
\begin{document}
\begin{todolist}
  \item Complete the assignment
  \item Review the lecture notes
  \item Prepare for the exam
\end{todolist}
\end{document}
```

[![TODO List example](https://github.com/LucaCappelletti94/lectures/blob/master/todolist.png?raw=true)](https://github.com/LucaCappelletti94/lectures/blob/master/todolist.png)

### Additional gimmicks

- When a page is empty, Latex won't generate page number or other page elements.
- When you want to leave a blank line you can just leave a blank line, without adding `\\`.
- If you'd like to use roman numerals there a command for that: `\rom{your number goes here}`.

