---
layout: proof
mathjax: true

author: "Joram Soch"
affiliation: "OvGU Magdeburg"
e_mail: "joram.soch@ovgu.de"
date: 2026-06-14 16:13:00

title: "Derivation of the group log Bayes factor"
chapter: "Model Selection"
section: "Bayesian model selection"
topic: "Bayes factor"
theorem: "Derivation of the group log Bayes factor"

sources:
  - authors: "Soch J, Allefeld C"
    year: 2018
    title: "MACS – a new SPM toolbox for model assessment, comparison and selection"
    in: "Journal of Neuroscience Methods"
    pages: "vol. 306, pp. 19-31, eqs. 19-20"
    url: "https://www.sciencedirect.com/science/article/pii/S0165027018301468"
    doi: "10.1016/j.jneumeth.2018.05.017"

proof_id: "P544"
shortcut: "glbf-der"
username: "JoramSoch"
---


**Theorem:** Let there be two [generative models](/D/gm) $m_1$ and $m_2$ for a set of $N$ [conditionally independent](/D/ind-cond) [data sets](/D/data) $Y = \left\lbrace y_1, \ldots, y_N \right\rbrace$ with [model evidences](/D/ml) $p(y_i \vert m_1)$ and $p(y_i \vert m_2)$ for $i = 1,\ldots,N$. Then, the [group log Bayes factor](/D/glbf)

$$ \label{eq:glbf-gbf}
\mathrm{GLBF}_{12} = \log \mathrm{GBF}_{12}
$$

can be expressed as

$$ \label{eq:glbf-lme}
\mathrm{GLBF}_{12} = \sum_{i=1}^N \left[ \log p(y_i \vert m_1) - \log p(y_i \vert m_2) \right] \; .
$$

or

$$ \label{eq:glbf-lbf}
\mathrm{GLBF}_{12} = \sum_{i=1}^N \mathrm{LBF}_{12}^{(i)}
$$

where $\mathrm{LBF}_{12}^{(i)}$ is the [log Bayes factor](/D/lbf) for $y_i$ in favor of $m_1$ over $m_2$.


**Proof:**

1) The [group Bayes factor](/D/gbf) for the "group data set" $Y$ [is equal to](/P/gbf-der)

$$ \label{eq:gbf-me}
\mathrm{GBF}_{12} = \prod_{i=1}^N \frac{p(y_i \vert m_1)}{p(y_i \vert m_2)} \; .
$$

Logarithmizing both sides of \eqref{eq:gbf-me}, we get:

$$ \label{eq:glbf-lme-qed}
\begin{split}
\log \mathrm{GBF}_{12} &= \log \prod_{i=1}^N \frac{p(y_i \vert m_1)}{p(y_i \vert m_2)} \\
\mathrm{GLBF}_{12} &= \sum_{i=1}^N \log \frac{p(y_i \vert m_1)}{p(y_i \vert m_2)} \\
\mathrm{GLBF}_{12} &= \sum_{i=1}^N \left[ \log p(y_i \vert m_1) - \log p(y_i \vert m_2) \right] \; .
\end{split}
$$

2) The [log Bayes factor](/D/lbf) for a "single data set" $y_i$ [evaluates to](/P/lbf-lme)

$$ \label{eq:lbf-lme-yi}
\mathrm{LBF}_{12}^{(i)} = \log p(y_i \vert m_1) - \log p(y_i \vert m_2)
$$

and substituting \eqref{eq:lbf-lme-yi} into \eqref{eq:glbf-lme-qed}, we obtain:

$$ \label{eq:glbf-lbf-qed}
\mathrm{GLBF}_{12} = \sum_{i=1}^N \mathrm{LBF}_{12}^{(i)} \; .
$$