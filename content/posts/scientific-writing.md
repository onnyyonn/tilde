---
author: "onnyyonn"
title: "Scientific Writing"
date: "2022-06-08"
description:
tags:
ShowToc: true
TocOpen: true
Katex: true
TikZ: true
---
## Katex

### Inline Mode

Equation: $x^2 + y^2 = z^2$

### Display mode

$$
x^2 + y^2 = z^2
$$

## TikZ

<script type="text/tikz">
  \begin{tikzpicture}
    \draw (0,0) circle (1in);
  \end{tikzpicture}
</script>

<script type="text/tikz">
  \begin{tikzpicture}[
  roundnode/.style={circle, draw=green!60, fill=green!5, very thick, minimum size=7mm},
  squarednode/.style={rectangle, draw=red!60, fill=red!5, very thick, minimum size=5mm},
  ]
  %Nodes
  \node[squarednode]      (maintopic)                              {2};
  \node[roundnode]        (uppercircle)       [above=of maintopic] {1};
  \node[squarednode]      (rightsquare)       [right=of maintopic] {3};
  \node[roundnode]        (lowercircle)       [below=of maintopic] {4};
  
  %Lines
  \draw[->] (uppercircle.south) -- (maintopic.north);
  \draw[->] (maintopic.east) -- (rightsquare.west);
  \draw[->] (rightsquare.south) .. controls +(down:7mm) and +(right:7mm) .. (lowercircle.east);
  \end{tikzpicture}
</script>


	
