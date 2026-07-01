---
layout: definition
mathjax: true

author: "Joram Soch"
affiliation: "OvGU Magdeburg"
e_mail: "joram.soch@ovgu.de"
date: 2026-06-04 17:32:00

title: "Group log Bayes factor"
chapter: "Model Selection"
section: "Bayesian model selection"
topic: "Bayes factor"
definition: "Group log Bayes factor"

sources:
  - authors: "Soch J, Allefeld C"
    year: 2018
    title: "MACS – a new SPM toolbox for model assessment, comparison and selection"
    in: "Journal of Neuroscience Methods"
    pages: "vol. 306, pp. 19-31, eq. 20"
    url: "https://www.sciencedirect.com/science/article/pii/S0165027018301468"
    doi: "10.1016/j.jneumeth.2018.05.017"

def_id: "D234"
shortcut: "glbf"
username: "JoramSoch"
---


**Definition:** Let there be two [generative models](/D/gm) $m_1$ and $m_2$ which are mutually exclusive, but not necessarily collectively exhaustive:

$$ \label{eq:m12}
\neg (m_1 \land m_2)
$$

Then, the group Bayes factor for a group data set $Y = \left\lbrace y_1, \ldots, y_N \right\rbrace$ in favor of $m_1$ and against $m_2$ is the product of the [Bayes factors](/D/bf) across all units of the group:

$$ \label{eq:gbf}
\mathrm{GBF}_{12} = \prod_{i=1}^N \frac{p(y_i \vert m_1)}{p(y_i \vert m_2)} \; .
$$

The group log Bayes factor is given by the logarithm of the group Bayes factor:

$$ \label{eq:glbf}
\mathrm{GLBF}_{12} = \log \mathrm{GBF}_{12} = \sum_{i=1}^N \log \frac{p(y_i|m_1)}{p(y_i|m_2)} \; .
$$