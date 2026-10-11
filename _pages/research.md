---
layout: single
title: "Research"
permalink: /research/
author_profile: true
toc: true
toc_label: "On this page"
---

Flexible models such as Bayesian additive regression trees (BART) are widely used for prediction and treatment-effect estimation. However, their computational convenience rests on a Gaussian error model. When data have heavy tails or outliers, as health and observational data often do, that assumption can distort both predictions and statements of uncertainty. My research develops methods that remain reliable when conventional distributional assumptions fail, and that are honest about what they cannot do.

## Dissertation: Robust Bayesian Tree Models

**Approximate Empirical Likelihood BART (AEL-BART)**

Empirical likelihood builds likelihood-type inference from estimating equations without a fully specified error distribution. Applied globally to BART, though, it cannot tell competing tree partitions apart. The key idea of AEL-BART is to **localize empirical likelihood within the terminal nodes of each tree**:

- A Huber-type estimating equation in each node limits the influence of extreme residuals.
- A Laplace approximation gives a closed-form score that fits into BART's usual backfitting algorithm.
- Robustness is data-dependent. Leaves dominated by outliers receive less effective precision, while well-behaved leaves behave much like standard BART.
- Split-conformal calibration gives prediction intervals with finite-sample marginal coverage, without assuming an error distribution.

**What the simulations show.** As error tails grow heavier, AEL-BART increasingly outperforms BART. With *n* = 300 and *t*<sub>3</sub> errors, its RMSE is 0.153 versus 0.279 for BART with one covariate. The simulations also show limits. Near-Gaussian errors carry an efficiency cost, and credible intervals tend to over-cover. Those findings set my next steps.

*Kuetsinya, C., & Ning, W. Approximate Empirical Likelihood-based Bayesian Additive Regression Trees. Submitted to* Statistical Science.

## Current and Future Directions

- **Adaptive robustness.** Data-dependent robustness that responds to the observed tail heaviness and asymmetry, protecting against outliers when needed and recovering BART's efficiency when not.
- **Calibrated uncertainty.** Sample-size-adaptive prior scaling to fix over-coverage, and locally adaptive conformal intervals that are narrower where prediction is easy and wider where it is hard.
- **Robust causal inference.** Extending localized empirical likelihood to Bayesian causal forests for heterogeneous treatment effects.
- **Sensitivity analysis for unmeasured confounding.** Benchmarking methods that combine E-values with negative controls.
- **AI in statistics education.** Evaluating how large language models perform in statistical instruction and how they can be integrated into courses responsibly.

## Applied Collaboration

- **Community nutrition and hypertension.** Statistical analysis for the Break Up with Salt program, published in the *International Journal of Environmental Research and Public Health* (2024).
- **Southern Pine Beetle infestations.** As a statistical consultant at LSU, I worked with Dr. Todd D. Johnson and the USDA Forest Service to model infestation dynamics after prescribed burns in two Mississippi national forests. I presented this work at two regional conferences in 2023.
- **Statistical consulting.** At LSU's Department of Experimental Statistics, I helped faculty and students across departments design and analyze studies using R, SAS, and Python.

## Projects for Students

Much of my research runs on simulation and computation that undergraduates can own. Each project below fits a summer or an independent study and can grow into a senior capstone.

- **Robustness under pressure.** Compare BART and AEL-BART across error distributions. *Needs: intro statistics and some R.*
- **Do prediction intervals keep their promises?** Test how conformal intervals behave when standard assumptions are violated. *Needs: intro statistics and some R.*
- **How strong would a hidden confounder need to be?** Apply sensitivity analysis to a published public health finding. *Needs: interest in causal questions and some R.*
- **From research code to software.** Turn simulation code into a documented, tested R package. *Needs: programming experience.*
- **Methodological extensions.** Contribute to the adaptive robustness work. *Needs: calculus-based probability and statistics.*

Students interested in working together are welcome to [email me](mailto:ckuetsinya@gmail.com).
