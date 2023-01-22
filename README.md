# LaTeX Template

Not only a LaTeX template, but also a study note.

- [LaTeX setup](https://jacobbishopxy.github.io/docs/2022-12-3-latex-setup/)

- [LaTeX multi-file projects](https://www.overleaf.com/learn/latex/Multi-file_LaTeX_projects)

- [LaTeX code listings](https://nasa.github.io/nasa-latex-docs/html/examples/listing.html)

- [TiKz website](https://tikz.net/): LaTeX graphics package

- [TiKz tutorial](https://www.overleaf.com/learn/latex/LaTeX_Graphics_using_TikZ%3A_A_Tutorial_for_Beginners_(Part_1)%E2%80%94Basic_Drawing)

- [GeoGebra](https://www.geogebra.org/): generating TiKz Code

## Content

### Sub-files

[main.tex] and all the sub-files in sections folder.

main:

```tex
\usepackage{subfiles}
```

sub:

```tex
\documentclass[../main.tex]{subfiles}
```

### Embeded PNG

[introduction.tex](./sections/introduction.tex):

main:

```tex
\graphicspath{\subfix{./images/}}
```

sub:

```tex
\graphicspath{{\subfix{../images/}}}

\begin{figure}[bh]
  \centering
  \includegraphics[width=3cm]{\subfix{../images/Yelan}}

  \label{fig:yelan}
  \caption{Yelan}
\end{figure}
```

PS: The reason why used different `\graphicspath` in main and sub is there relative import's locations are different. Furthermore, since we are in the sub-file mode, which implies each sub-file can be compiled individually, hence including images file seperately is very neccessay.

### Custom commands

[commands.tex](commands.tex): customized commands, can be use anywhere because it is imported in the main file by `\input{commands}`.

### Custom styling

[style.sty](./style.sty): style file, affects all the related line or blocks (imported in the main file by `\usepackage{./style}` and `\lstset{style=mystyle}`).

### TiKz tutorial

LaTeX Graphics
