---
layout: definition
mathjax: true

author: "Joram Soch"
affiliation: "OvGU Magdeburg"
e_mail: "joram.soch@ovgu.de"
date: 2026-06-04 17:23:00

title: "Group Bayes factor"
chapter: "Model Selection"
section: "Bayesian model selection"
topic: "Bayes factor"
definition: "Group Bayes factor"

sources:
  - authors: "Stephan KE, Penny WD, Daunizeau J, Moran RJ, Friston KJ"
    year: 2009
    title: "Bayesian model selection for group studies"
    in: "NeuroImage"
    pages: "vol. 46, pp. 1004–1017, eq. 2"
    url: "https://www.sciencedirect.com/science/article/abs/pii/S1053811909002638"
    doi: "10.1016/j.neuroimage.2009.03.025"
  - authors: "Penny WD, Stephan KE, Daunizeau J, Rosa MJ, Friston KJ, Schofield TM, Leff AP"
    year: 2010
    title: "Comparing Families of Dynamic Causal Models"
    in: "PLoS Computational Biology"
    pages: "vol. 6, iss. 3, art. e1000709, eqs. 6/8"
    url: "https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1000709"
    doi: "10.1371/journal.pcbi.1000709"
  - authors: "Soch J, Allefeld C"
    year: 2018
    title: "MACS – a new SPM toolbox for model assessment, comparison and selection"
    in: "Journal of Neuroscience Methods"
    pages: "vol. 306, pp. 19-31, eq. 20"
    url: "https://www.sciencedirect.com/science/article/pii/S0165027018301468"
    doi: "10.1016/j.jneumeth.2018.05.017"

def_id: "D233"
shortcut: "gbf"
username: "JoramSoch"
---


**Definition:** Let $Y = \left\lbrace y_1, \ldots, y_N \right\rbrace$ be a set of $N$ [data sets](/D/data) (forming a "group") and consider two [generate models](/D/gm) $m_1$ and $m_2$ with [model evidences](/D/ml) (i.e. marginal likelihoods) $p(y_i \vert m)$ where $i = 1,\ldots,N$ and $m \in \left\lbrace m_1, m_2 \right\rbrace$. Then, the group Bayes factor for $Y$ in favor of $m_1$ over $m_2$ is defined as:

$$ \label{eq:GBF}
\mathrm{GBF}_{12} = \prod_{i=1}^N \frac{p(y_i \vert m_1)}{p(y_i \vert m_2)} \; .
$$