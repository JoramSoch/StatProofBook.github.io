---
layout: proof
mathjax: true

author: "Joram Soch"
affiliation: "OvGU Magdeburg"
e_mail: "joram.soch@ovgu.de"
date: 2026-05-28 16:28:01

title: "Invariance of the correlation under linear transformation"
chapter: "General Theorems"
section: "Probability theory"
topic: "Correlation"
theorem: "Invariance under linear transformation"

sources:
  - authors: "Ostwald D, Soch J"
    year: 2026
    title: "Korrelation"
    in: "Allgemeines Lineares Modell"
    pages: "Einheit (2), Folien 13-14"
    url: "https://www.ipsy.ovgu.de/ipsy_media/Methodenlehre+I/Sommersemester+2026/Allgemeines+Lineares+Modell/02_Korrelation.pdf"

proof_id: "P541"
shortcut: "corr-inv"
username: "JoramSoch"
---


**Theorem:** Let $X$ and $Y$ be two [random variables](/D/rvar). Then, the correlation of any linear transformations of $X$ and $Y$ is equal to the correlation of $X$ and $Y$ up to a possible change in sign:

$$ \label{eq:corr-inv}
\mathrm{Corr}(aX+b,cY+d) = \pm \mathrm{Corr}(X,Y) \; .
$$


**Proof:** The [correlation](/D/corr) is defined in terms of [covariance](/D/cov) and [variance](/D/var) as

$$ \label{eq:corr}
\mathrm{Corr}(X,Y) = \frac{\mathrm{Cov}(X,Y)}{\sqrt{\mathrm{Var}(X)} \sqrt{\mathrm{Var}(Y)}} \; .
$$

The covariance is [invariant under addition](/P/cov-inv) and [scales upon multiplication](/P/cov-scal) with constants:

$$ \label{eq:cov-inv-scal}
\mathrm{Cov}(aX+b,cY+d) = a c \, \mathrm{Cov}(X,Y) \; .
$$

Variances are also [invariant under addition](/P/var-inv) and [scale upon multiplication](/P/var-scal) with constants:

$$ \label{eq:var-inv-scal}
\begin{split}
\mathrm{Var}(aX+b) &= a^2 \mathrm{Var}(X) \\
\mathrm{Var}(cY+d) &= c^2 \mathrm{Var}(Y) \; .
\end{split}
$$

Taking all this together, we obtain:

$$ \label{eq:corr-inv-qed}
\begin{split}
   \mathrm{Corr}(aX+b,cY+d)
&\overset{\eqref{eq:corr}}{=} \frac{\mathrm{Cov}(aX+b,cY+d)}{\sqrt{\mathrm{Var}(aX+b)} \sqrt{\mathrm{Var}(cY+d)}} \\
&\overset{\eqref{eq:cov-inv-scal}}{=} \frac{a c \, \mathrm{Cov}(X,Y)}{\sqrt{\mathrm{Var}(aX+b)} \sqrt{\mathrm{Var}(cY+d)}} \\
&\overset{\eqref{eq:var-inv-scal}}{=} \frac{a c \, \mathrm{Cov}(X,Y)}{\sqrt{a^2 \mathrm{Var}(X)} \sqrt{c^2 \mathrm{Var}(Y)}} \\
&= \frac{a c}{\sqrt{a^2} \sqrt{c^2}} \frac{\mathrm{Cov}(X,Y)}{\sqrt{\mathrm{Var}(X)} \sqrt{\mathrm{Var}(Y)}} \\
&= \frac{a c}{|a| |c|} \frac{\mathrm{Cov}(X,Y)}{\sqrt{\mathrm{Var}(X)} \sqrt{\mathrm{Var}(Y)}} \\
&\overset{\eqref{eq:corr}}{=} \pm \mathrm{Corr}(X,Y) \; .
\end{split}
$$