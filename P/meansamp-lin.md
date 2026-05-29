---
layout: proof
mathjax: true

author: "Joram Soch"
affiliation: "OvGU Magdeburg"
e_mail: "joram.soch@ovgu.de"
date: 2026-05-28 08:52:30

title: "Linearity of the sample mean"
chapter: "General Theorems"
section: "Probability theory"
topic: "Expected value"
theorem: "Linearity of the sample mean"

sources:

proof_id: "P538"
shortcut: "meansamp-lin"
username: "JoramSoch"
---


**Theorem:** Let $x = \left\lbrace x_1, \ldots, x_n \right\rbrace$ be a [sample](/D/samp) from a [random variable](/D/rvar) $X$ and let $\tilde{x} = \left\lbrace \tilde{x}_1, \ldots, \tilde{x}_n \right\rbrace$ be a linearly transformed version of this sample with

$$ \label{eq:samp-lin}
\tilde{x}_i = a x_i + b \; .
$$

where $a$ and $b$ are constant real numbers. The [sample mean](/D/samp-mean) behaves linearly under this transformation, i.e.

$$ \label{eq:mean-samp-lin}
\bar{\tilde{x}} = a \bar{x} + b \; .
$$


**Proof:** The [sample mean](/D/mean-samp) is defined as

$$ \label{eq:mean-samp}
\bar{x} = \frac{1}{n} \sum_{i=1}^{n} x_i \; .
$$

Applying this definition to the linearly transformed sample, we obtain:

$$ \label{eq:mean-samp-lin-qed}
\begin{split}
   \bar{\tilde{x}}
&\overset{\eqref{eq:mean-samp}}{=} \frac{1}{n} \sum_{i=1}^{n} \tilde{x}_i \\
&\overset{\eqref{eq:samp-lin}}{=} \frac{1}{n} \sum_{i=1}^{n} (a x_i + b) \\
&= \frac{1}{n} \sum_{i=1}^{n} a x_i + \frac{1}{n} \sum_{i=1}^{n} b \\
&= a \cdot \frac{1}{n} \sum_{i=1}^{n} x_i + \frac{1}{n} \cdot n b \\
&= a \bar{x} + b \; .
\end{split}
$$