---
layout: post
title: Example Content III
description: >
  A page showing Hydejack-specific markdown content.
image: 
  path: /assets/img/blog/example-content-iii.jpg
  srcset:
    1060w: /assets/img/blog/example-content-iii.jpg
    530w:  /assets/img/blog/example-content-iii@0,5x.jpg
    265w:  /assets/img/blog/example-content-iii@0,25x.jpg
related_posts:
  - example/_posts/2017-11-23-example-content-ii.md
  - /example/2012-02-07-example-content/
sitemap: false
---

## March 2022

* Contributors are invited to Google Summer of Code (GSoC) - 2022 !!!
  * There are two project proposals related to time series analysis submitted in GSOC-2022 with the organization, '[R Project for Statistical Computing](https://github.com/rstats-gsoc/gsoc2022/wiki)'.
  * The descriptions of these projects are as follows:
     * [imputeTestbenchG: imputation testbench for Genomics data](https://github.com/rstats-gsoc/gsoc2022/wiki/imputeTestbenchG%3A-imputation-testbench-for-Genomics-data) (Co-mentor: Mogens Sandø Lund, Director, and Head of Center for Quantitative Genetics and Genomics, Aarhus University, Denmark).
     * [VedicDateTime](https://github.com/rstats-gsoc/gsoc2022/wiki/VedicDateTime) (Co-mentor: TBA).
  * The structure, benefits, and other details of the GSoC can be found at: https://developers.google.com/open-source/gsoc/resources/downloads/GSoC2021Flyer.pdf
  * Contributors are welcome to participate in GSoC-2022 by submitting the tests provided on the respective project wiki page. 

## Code blocks

~~~js
// Example can be run directly in your JavaScript console

// Create a function that takes two arguments and returns the sum of those
// arguments
var adder = new Function("a", "b", "return a + b");

// Call the function
adder(2, 6);
// > 8
~~~


## Math
Lorem ipsum $$ f(x) = x^2 $$.

$$
\begin{aligned}
  \phi(x,y) &= \phi \left(\sum_{i=1}^n x_ie_i, \sum_{j=1}^n y_je_j \right) \\[2em]
            &= \sum_{i=1}^n \sum_{j=1}^n x_i y_j \phi(e_i, e_j)            \\[2em]
            &= (x_1, \ldots, x_n)
               \left(\begin{array}{ccc}
                 \phi(e_1, e_1)  & \cdots & \phi(e_1, e_n) \\
                 \vdots          & \ddots & \vdots         \\
                 \phi(e_n, e_1)  & \cdots & \phi(e_n, e_n)
               \end{array}\right)
               \left(\begin{array}{c}
                 y_1    \\
                 \vdots \\
                 y_n
               \end{array}\right)
\end{aligned}
$$


## Message boxes
**NOTE**: You can add a message box.
{:.message}

## Large text
You can add large text.
{:.lead}

## Large images
![Full-width image](https://placehold.it/800x100){:.lead data-width="800" data-height="100"}

## Captions to images
![Full-width image](https://placehold.it/800x100){:.lead data-width="800" data-height="100"}
A caption to an image.
{:.figure}

## Large quotes
> You can make a quote "pop out".
{:.lead}

## Faded text
I'm faded, faded, faded.
{:.faded}


[mm]: https://guides.github.com/features/mastering-markdown/
[ksyn]: https://kramdown.gettalong.org/syntax.html
[ksyntab]:https://kramdown.gettalong.org/syntax.html#tables
[ksynmath]: https://kramdown.gettalong.org/syntax.html#math-blocks
[katex]: https://khan.github.io/KaTeX/
[rtable]: https://dbushell.com/2016/03/04/css-only-responsive-tables/
