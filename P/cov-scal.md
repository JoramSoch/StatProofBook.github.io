---
layout: proof
mathjax: true

author: "Joram Soch"
affiliation: "OvGU Magdeburg"
e_mail: "joram.soch@ovgu.de"
date: 2026-05-28 10:36:32

title: "Scaling of the covariance upon multiplication with constants"
chapter: "General Theorems"
section: "Probability theory"
topic: "Covariance"
theorem: "Scaling upon multiplication"

sources:

proof_id: "P540"
shortcut: "cov-scal"
username: "JoramSoch"
---


**Theorem:** The [covariance](/D/var) scales upon multiplication with [constants](/D/const):

$$ \label{eq:cov-scal}
\mathrm{Cov}(aX,bY) = a b \, \mathrm{Cov}(X,Y) \; .
$$


**Proof:** The [covariance](/D/var) is defined in terms of the [expected value](/D/mean) as

$$ \label{eq:cov}
\mathrm{Cov}(X,Y) = \mathrm{E}\left[ (X-\mathrm{E}(X)) (Y-\mathrm{E}(Y)) \right] \; .
$$

Using this and the [linearity of the expected value](/P/mean-lin), we can derive \eqref{eq:cov-scal} as follows:

$$ \label{eq:cov-scal-qed}
\begin{split}
   \mathrm{Cov}(aX,bY)
&\overset{\eqref{eq:cov}}{=} \mathrm{E}\left[ ((aX)-\mathrm{E}(aX)) ((bY)-\mathrm{E}(bY)) \right] \\
&= \mathrm{E}\left[ (aX-a\mathrm{E}(X)) (bY-b\mathrm{E}(Y)) \right] \\
&= \mathrm{E}\left[ a (X-\mathrm{E}(X)) b (Y-\mathrm{E}(Y)) \right] \\
&= a b \, \mathrm{E}\left[ (X-\mathrm{E}(X)) (Y-\mathrm{E}(Y)) \right] \\
&\overset{\eqref{eq:cov}}{=} a b \, \mathrm{Cov}(X,Y) \; . \\
\end{split}
$$