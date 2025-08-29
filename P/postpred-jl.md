---
layout: proof
mathjax: true

author: "Osvaldo Martin"
affiliation: "Universidad Nacional de San Martín"
e_mail: "aloctavodia@gmail.com"
date: 2024-09-11 15:30:00

title: "Posterior predictive distribution is a marginal distribution of the joint likelihood"
chapter: "General Theorems"
section: "Bayesian statistics"
topic: "Probabilistic modeling"
theorem: "Posterior predictive distribution is marginal of joint likelihood"

sources:

proof_id: "P467"
shortcut: "postpred-jl"
username: "aloctavodia"
---


**Theorem:** The [posterior predictive distribution](/D/post-pred) is the [marginal distribution](/D/dist-marg) of the [joint likelihood](/D/ml) of the [new data](/D/data) $y_{\mathrm{new}}$, conditional on the measured data $y$:

$$ \label{eq:postpred-jl}
p(y_{\mathrm{new}} \vert y) = \int p(y_{\mathrm{new}}, \theta \vert y) \, \mathrm{d}\theta
$$


**Proof:** The [posterior predictive distribution](/D/post-pred) is defined as the [marginal distribution](/D/dist-marg) of new data $y_{\mathrm{new}}$, predicted based on the [posterior distribution](/D/post) obtained from the measured data $y$:

$$ \label{eq:post-pred-s1}
p(y_{\mathrm{new}} \vert y) = \int p(y_{\mathrm{new}} \vert \theta) \, p(\theta \vert y) \, \mathrm{d}\theta \; .
$$

We notice that $y_{\text{new}}$ is [independent](/P/prob-ind) of $y$, so we can write:

$$ \label{eq:post-pred-s2}
p(y_{\mathrm{new}} \vert y) = \int p(y_{\mathrm{new}} \vert \theta, y) \, p(\theta \vert y) \, \mathrm{d}\theta \; .
$$

By using the [law of conditional probability](/D/prob-cond), we can write the integrand as:

$$ \label{eq:jl-post}
p(y_{\text{new}} \vert \theta, y) \, p(\theta \vert y) = p(y_{\text{new}}, \theta \vert y) \; .
$$

This is the [posterior](/D/post) [joint likelihood](/D/jl). Thus, expression \eqref{eq:post-pred-s1} can be written as:

$$ \label{eq:postpred-jl-qed}
p(y_{\mathrm{new}} \vert y) = \int p(y_{\mathrm{new}}, \theta \vert y) \, \mathrm{d}\theta \; .
$$