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

Example 1:
<script type="text/tikz">
  \begin{tikzpicture}
    \filldraw[color=red!60, fill=red!5, very thick](-1,0) circle (1.5);
    \draw[blue, very thick] (0,0) rectangle (3,2);
    \draw[orange, ultra thick] (4,0) -- (6,0) -- (5.7,2) -- cycle;
  \end{tikzpicture}
</script>

Example 2:
<script type="text/tikz">
  \tikzstyle{process}=[draw, rectangle, rounded corners, fill=yellow!20, minimum width=3cm, minimum height=1cm]
  \tikzstyle{decision}=[draw, diamond, fill=red!20, minimum width=4cm, aspect=2]
  \tikzstyle{arrow}=[white, thick,->,>=stealth]
  \node[process] (waking) at (0,0) {Wake up};
  \node[decision] (day) at (0,-3) {Is it a weekday?};
  \node[process] (up) at (0,-6) {Get out of bed};
  \node[process] (sleep) at (5,-3) {Go back to sleep};
  \draw[arrow] (waking) -- (day);
  \draw[arrow] (day) -- node[anchor=east] {Yes} (up);
  \draw[arrow] (day) --node[anchor=south] {No} (sleep);
  \draw[arrow] (sleep) |- (waking);
</script>


	
