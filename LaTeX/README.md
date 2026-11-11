# LaTeX

## What is LaTeX?
LaTeX is a document preparation system commonly used for technical and scientific documents containing equations, tables, figures, and references.

## Basic structure
```latex
\documentclass{article}
\begin{document}
Hello, LaTeX!
\end{document}
```
- `\documentclass{article}` selects the document type.
- The preamble is before `\begin{document}`.
- Document content is between `\begin{document}` and `\end{document}`.

## Common classes
- `article`: short documents and assignments.
- `report`: longer reports.
- `book`: book-length documents.
- `letter`: letters.

## Text formatting and sections
```latex
\textbf{Bold}
\textit{Italic}
\underline{Underlined}
```
Use `\section{}`, `\subsection{}`, and `\subsubsection{}` for headings.

## Lists
```latex
\begin{itemize}
  \item First point
  \item Second point
\end{itemize}

\begin{enumerate}
  \item First step
  \item Second step
\end{enumerate}
```

## Mathematics
Inline: `\(a^2+b^2=c^2\)`

Displayed:
```latex
\[
E = mc^2
\]
```
Numbered:
```latex
\begin{equation}
F = ma
\end{equation}
```

## Tables
```latex
\begin{tabular}{|c|c|}
\hline
Name & Marks \\
\hline
Asha & 90 \\
Ravi & 85 \\
\hline
\end{tabular}
```

## Figures
Add `\usepackage{graphicx}` in the preamble:
```latex
\begin{figure}[h]
  \centering
  \includegraphics[width=0.6\textwidth]{image.png}
  \caption{Example figure}
  \label{fig:example}
\end{figure}
```

## References
Use `\label{}` to mark an item and `\ref{}` to refer to it. Bibliographies can use a `.bib` file with BibTeX or another bibliography workflow.

## Compile
A common command is `pdflatex main.tex`. Some documents need multiple compilation passes or a bibliography tool.

## Checklist
- Put packages in the preamble.
- Close every environment correctly.
- Escape special characters such as `#`, `$`, `%`, `&`, `_`, `{`, and `}` when used as text.
- Compile and inspect the PDF.

> Introductory general notes: follow the lab handout for required packages, compiler, and formatting.
