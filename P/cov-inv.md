---
layout: proof
mathjax: true

author: "Joram Soch"
affiliation: "OvGU Magdeburg"
e_mail: "joram.soch@ovgu.de"
date: 2026-05-28 10:25:49

title: "Invariance of the covariance under addition of constants"
chapter: "General Theorems"
section: "Probability theory"
topic: "Covariance"
theorem: "Invariance under addition"

sources:

proof_id: "P539"
shortcut: "cov-inv"
username: "JoramSoch"
---


**Theorem:** The [covariance](/D/cov) is invariant under addition of [constants](/D/const):

$$ \label{eq:cov-inv}
\mathrm{Cov}(X+a,Y+b) = \mathrm{Cov}(X,Y) \; .
$$


**Proof:** The [covariance](/D/cov) is defined in terms of the [expected value](/D/mean) as

$$ \label{eq:cov}
\mathrm{Cov}(X,Y) = \mathrm{E}\left[ (X-\mathrm{E}(X)) (Y-\mathrm{E}(Y)) \right] \; .
$$

Using this and the [linearity of the expected value](/P/mean-lin), we can derive \eqref{eq:cov-inv} as follows:

$$ \label{eq:cov-inv-qed}
\begin{split}
   \mathrm{Cov}(X+a,Y+b)
&\overset{\eqref{eq:cov}}{=} \mathrm{E}\left[ ((X+a)-\mathrm{E}(X+a)) ((Y+b)-\mathrm{E}(Y+b)) \right] \\
&= \mathrm{E}\left[ (X + a - \mathrm{E}(X) - a) (Y + b - \mathrm{E}(Y) - b) \right] \\
&= \mathrm{E}\left[ (X-\mathrm{E}(X)) (Y-\mathrm{E}(Y)) \right] \\
&\overset{\eqref{eq:cov}}{=} \mathrm{Cov}(X,Y) \; . \\
\end{split}
$$