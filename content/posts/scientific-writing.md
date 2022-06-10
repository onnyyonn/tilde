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
    \filldraw[color=red!60, fill=red!5, very thick](-1,0) circle (1.5);
    \draw[blue, very thick] (0,0) rectangle (3,2);
    \draw[orange, ultra thick] (4,0) -- (6,0) -- (5.7,2) -- cycle;
  \end{tikzpicture}
</script>

<script type="text/tikz">
  \begin{tikzpicture}
	  %Nodes
	  \node[rectangle, draw=red!60, fill=red!5, very thick, minimum size=5mm]      (maintopic)                              {2};
	  \node[circle, draw=green!60, fill=green!5, very thick, minimum size=7mm]     (uppercircle)       [above=of maintopic] {1};
	  \noderectangle, draw=red!60, fill=red!5, very thick, minimum size=5mm]       (rightsquare)       [right=of maintopic] {3};
	  \node[circle, draw=green!60, fill=green!5, very thick, minimum size=7mm]     (lowercircle)       [below=of maintopic] {4};
	  
	  %Lines
	  \draw[->] (uppercircle.south) -- (maintopic.north);
	  \draw[->] (maintopic.east) -- (rightsquare.west);
	  \draw[->] (rightsquare.south) .. controls +(down:7mm) and +(right:7mm) .. (lowercircle.east);
  \end{tikzpicture}
</script>


	
