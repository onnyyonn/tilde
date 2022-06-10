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
  \begin{tikzpicture}
	  \draw (0,0) -- (12,0);
	  \draw (0.2,1)node[left,font=\tiny] {$y=1$} -- (11.8,1);
	  \draw (0.2,-1)node[left,font=\tiny] {$y=-1$} -- (11.8,-1); 
	  \foreach \x in {0,0.5,...,12}{
	    \draw (\x,-0.2)node [below,font=\tiny,] {\x} -- (\x,0.2) ;
	  }
	  \draw[ultra thick, red]
	      (3,0) sin (4,1) cos (5,0) sin (6,-1) cos (7,0)
	            sin (8,1) cos (9,0) sin (10,-1) cos (11,0);    
  \end{tikzpicture}
</script>

## Kroki

{{< kroki type="actdiag" >}}
{
  write -> convert -> image

  lane user {
    label = "User"
    write [label = "Writing reST"];
    image [label = "Get diagram IMAGE"];
  }
  lane actdiag {
    convert [label = "Convert reST to Image"];
  }
}
{{< /kroki >}}

	
