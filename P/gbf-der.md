---
layout: proof
mathjax: true

author: "Joram Soch"
affiliation: "OvGU Magdeburg"
e_mail: "joram.soch@ovgu.de"
date: 2026-06-14 15:58:00

title: "Derivation of the group Bayes factor"
chapter: "Model Selection"
section: "Bayesian model selection"
topic: "Bayes factor"
theorem: "Derivation of the group Bayes factor"

sources:
  - authors: "Soch J, Allefeld C"
    year: 2018
    title: "MACS – a new SPM toolbox for model assessment, comparison and selection"
    in: "Journal of Neuroscience Methods"
    pages: "vol. 306, pp. 19-31, eqs. 19-20"
    url: "https://www.sciencedirect.com/science/article/pii/S0165027018301468"
    doi: "10.1016/j.jneumeth.2018.05.017"

proof_id: "P543"
shortcut: "gbf-der"
username: "JoramSoch"
---


**Theorem:** Let $Y = \left\lbrace y_1, \ldots, y_N \right\rbrace$ be a set of $N$ [conditionally independent](/D/ind-cond) [data sets](/D/data) given two [generate models](/D/gm) $m_1$ and $m_2$ with [model evidences](/D/ml) $p(y_i \vert m_1)$ and $p(y_i \vert m_2)$ for $i = 1,\ldots,N$. Then, the [group Bayes factor](/D/gbf) for $Y$ in favor of $m_1$ over $m_2$ can be expressed as

$$ \label{eq:gbf-me}
\mathrm{GBF}_{12} = \prod_{i=1}^N \frac{p(y_i \vert m_1)}{p(y_i \vert m_2)}
$$

or 

$$ \label{eq:gbf-bf}
\mathrm{GBF}_{12} = \prod_{i=1}^N \mathrm{BF}_{12}^{(i)} \; .
$$

where $\mathrm{BF}_{12}^{(i)}$ is the [Bayes factor](/D/bf) for $y_i$ in favor of $m_1$ over $m_2$.


**Proof:**

1) The [Bayes factor](/D/bf) for the "group data set" $Y$ evaluates to

$$ \label{eq:gbf-me-Y}
\mathrm{GBF}_{12} = \frac{p(Y \vert m_1)}{p(Y \vert m_2)} \; .
$$

Under [conditional independence](/D/ind-cond), we have

$$ \label{eq:p-Y-yi}
p(Y \vert m_1) = \prod_{i=1}^N p(y_i \vert m_1)
\quad \mathrm{and} \quad
p(Y \vert m_2) = \prod_{i=1}^N p(y_i \vert m_2)
$$

such that substituting \eqref{eq:p-Y-yi} into \eqref{eq:gbf-me-Y} gives:

$$ \label{eq:gbf-me-qed}
\mathrm{GBF}_{12} = \prod_{i=1}^N \frac{p(y_i \vert m_1)}{p(y_i \vert m_2)} \; .
$$

2) The [Bayes factor](/D/bf) for a "single data set" $y_i$ evaluates to

$$ \label{eq:bf-me-yi}
\mathrm{BF}_{12}^{(i)} = \frac{p(y_i \vert m_1)}{p(y_i \vert m_2)}
$$

and substituting \eqref{eq:bf-me-yi} into \eqref{eq:gbf-me-qed}, we obtain:

$$ \label{eq:gbf-bf-qed}
\mathrm{GBF}_{12} = \prod_{i=1}^N \mathrm{BF}_{12}^{(i)} \; .
$$