---
title: How it works
date: 2020-12-28
tags:
    - Algorithms
category: notes
keywords:
    - Algorithms
    - Graphs
mathjax: true
---

# How it works

### IPTW + Auto ML + whole EHR

The auto-epi methodology utilizes three key advances in epidemiological and machine learning methodology:
* Inverse probability treatment weighting (causal inference)
* Google Auto ML
* Whole EHR adjustment

Traditional observational epidemiology uses medical expertise to select likely confounders and manual coding to statistically or methodologically adjust for them. This is a time consuming and often difficult to reproduce process.

### Steps

We propose a methodology which automates much of this process while maintaining strong causal claims.

1. Define our exposure and outcomes of interest: e.g. Drug X and Disease Y.  
2. Use deep neural networks trained on whole EHR to assess the conditional probability of receiving treatment given EHR history.
3. Use IPTW to generate a randomized pseudo-population with respect to treatment.
4. Assess causal effect of treatment.
