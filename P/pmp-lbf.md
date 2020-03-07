---
layout: proof
mathjax: true

author: "Joram Soch"
affiliation: "BCCN Berlin"
e_mail: "joram.soch@bccn-berlin.de"
date: 2020-03-03 12:27:00

title: "Posterior model probability in terms of log Bayes factor"
chapter: "Model Selection"
section: "Bayesian model selection"
topic: "Log-evidence derivatives"
theorem: "Posterior model probability in terms of log Bayes factor"

sources:
  - authors: "Soch J, Allefeld C"
    year: 2018
    title: "MACS – a new SPM toolbox for model assessment, comparison and selection"
    in: "Journal of Neuroscience Methods"
    pages: "vol. 306, pp. 19-31, eq. 21"
    url: "https://www.sciencedirect.com/science/article/pii/S0165027018301468"
    doi: "10.1016/j.jneumeth.2018.05.017"

proof_id: "P73"
shortcut: "pmp-lbf"
username: "JoramSoch"
---


**Theorem:** Let $m_1$ and $m_2$ be two statistical models [log Bayes factor](/D/lbf) $\mathrm{LBF}_{1,2}$ in favor of model $m_1$ and against model $m_2$. Then, if both models are equally likely apriori, the [posterior model probability](/D/pmp) of $m_1$ is

$$ \label{eq:PMP-LBF}
p(m_1|y) = \frac{\exp(\mathrm{LBF}_{1,2})}{\exp(\mathrm{LBF}_{1,2}) + 1} \; .
$$


**Proof:** From [Bayes' rule](/P/bayes-rule), the posterior odds ratio is

$$ \label{eq:post-odds-s1}
\frac{p(m_1|y)}{p(m_2|y)} = \frac{p(y|m_1)}{p(y|m_2)} \cdot \frac{p(m_1)}{p(m_2)} \; .
$$

When both models are equally likely apriori, the prior odds ratio is one, such that

$$ \label{eq:post-odds-s2}
\frac{p(m_1|y)}{p(m_2|y)} = \frac{p(y|m_1)}{p(y|m_2)} \; .
$$

Now the right-hand side corresponds to the [Bayes factor](/D/bf), therefore

$$ \label{eq:post-odds-s4}
\frac{p(m_1|y)}{1-p(m_1|y)} = \mathrm{BF}_{1,2} \; .
$$

Because the two models are collectively exhaustive, we have

$$ \label{eq:post-odds-s3}
\frac{p(m_1|y)}{1-p(m_1|y)} = \mathrm{BF}_{1,2} \; .
$$

Now rearranging for the [posterior probability](/D/pmp), this gives

$$ \label{eq:post-s1}
p(m_1|y) = \frac{\mathrm{BF}_{1,2}}{\mathrm{BF}_{1,2} + 1} \; .
$$

Because the [log Bayes factor is the logarithm of the Bayes factor](/P/lbf-lme), we finally have

$$ \label{eq:post-s2}
p(m_1|y) = \frac{\exp(\mathrm{LBF}_{1,2})}{\exp(\mathrm{LBF}_{1,2}) + 1} \; .
$$