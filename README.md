# Latex Template

- [LaTeX setup](https://jacobbishopxy.github.io/docs/2022-12-3-latex-setup/)

- [VsCode settings for LaTeX](./VsCode_settings_for_LaTeX.json)

- [LaTeX Multi-file projects](https://www.overleaf.com/learn/latex/Multi-file_LaTeX_projects)

- [LaTeX Code Listings](https://nasa.github.io/nasa-latex-docs/html/examples/listing.html)

## Real LaTeX projects

- [studies-cpp](https://github.com/Jacobbishopxy/studies-cpp)

- [poma-notes](https://github.com/Jacobbishopxy/poma-notes)

## Note

- `commands.tex`: customized commands, can be use anywhere because it is imported in the main file by `\input{commands}`.

- `style.sty`: style file, affects all the related line or blocks (imported in the main file by `\usepackage{./style}` and `\lstset{style=mystyle}`).

- custom theorem style

  ```tex
  \newtheoremstyle{mytheoremstyle}                          % name
        {\topsep}                                           % Space above
        {\topsep}                                           % Space below
        {\itshape\fontfamily{ptm}\selectfont}               % Body font
        {}                                                  % Indent amount
        {\fontfamily{ptm}\selectfont\scshape\color{blue}}   % Theorem head font
        {:}                                                 % Punctuation after theorem head
        {.5em}                                              % Space after theorem head
        {}                                                  % Theorem head spec
  ```

  Theorem head spec: can be left empty, meaning ‘normal’
