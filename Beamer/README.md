# Beamer

## What is Beamer?
Beamer is a LaTeX document class for creating slide presentations. Each slide is usually written inside a `frame` environment.

## Minimal presentation
```latex
\documentclass{beamer}
\title{My Presentation}
\author{Student Name}
\institute{MNIT Jaipur}
\date{\today}

\begin{document}
\begin{frame}
  \titlepage
\end{frame}

\begin{frame}{Introduction}
  This is my first slide.
\end{frame}
\end{document}
```

## Important commands
- `\title{}`, `\author{}`, `\institute{}`, `\date{}`: presentation details.
- `\begin{frame}{Title}`: starts a slide.
- `\titlepage`: displays the title slide.
- `\frametitle{}`: sets a frame title.

## Lists
```latex
\begin{frame}{Objectives}
  \begin{itemize}
    \item Understand the topic
    \item Study an example
  \end{itemize}
\end{frame}
```
Use `enumerate` for numbered lists.

## Themes
Choose a theme in the preamble, for example `\usetheme{Madrid}`.

## Columns
```latex
\begin{frame}{Two columns}
  \begin{columns}
    \column{0.48\textwidth}
    Left-side content
    \column{0.48\textwidth}
    Right-side content
  \end{columns}
\end{frame}
```

## Images
Add `\usepackage{graphicx}` in the preamble:
```latex
\begin{frame}{Diagram}
  \includegraphics[width=0.7\textwidth]{diagram.png}
\end{frame}
```

## Overlays
```latex
\begin{itemize}
  \item<1-> First point
  \item<2-> Second point
\end{itemize}
```
The overlay specifications reveal content in stages.

## Compile and design tips
A common command is `pdflatex slides.tex`. Keep one main idea per slide, use readable text, avoid overcrowding, and inspect the compiled PDF.

> Introductory general notes: use the theme and structure required by your instructor if specified.
