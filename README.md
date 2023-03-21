# Examining substitution rates and ancestor dates with BEAST

This tutorial requires prior installation of Tracer (downloaded from https://github.com/beast-dev/tracer/releases) and FigTree (downloaded from https://github.com/rambaut/figtree/releases)

In this tutorial, we will analyse the output from BEAST analyses of two pandemic variants of norovirus, a highly prevalent cause of gastroenteritis. We aim to:
1) Identify the substitution rate of each variant
2) Compare the substitution rates between variants
3) Examine ancestor dates to make inferences about the drivers of pandemic spread

We will first use Tracer to examine the output from previous BEAST runs. BEAST outputs log files that contain the estimates of various parameters from the MCMC chain. Tracer summarises these log files to enable examination of posterior parameter estimates

When you open Tracer, you should see a window similar to this:

<img src="_figures/tracer_initial.png" width = "500">

To load a log file, click the plus sign in the top left corner (below "No file selected"). Open "Sydney.log" which contains the output from BEAST runs on sequences from the Sydney 2012 norovirus variant. This variant caused a pandemic in 2012. Tracer should now look like this:

<img src="_figures/tracer_loaded.png" width = "500">

The parameters of the model that we can examine within Tracer are shown on the left. The "posterior" is selected by default - this is the posterior probability of the model. The right hand window shows a summary of the selected parameter, including the mean and median estimates, confidence intervals and a plot of the posterior distribution of the parameter

The first thing we need to check when we load a log file is whether the MCMC chain has converged. If it hasn't, we can't currently analyse the output as the estimates may not be reliable. We assess convergence by examining the effective sample size (ESS) scores, which are the number of effectively independent draws from the posterior distribution that the Markov chain is equivalent to

We want the ESS scores to be as large as possible. 200 is usually used as the minimum cutoff. If one or more ESS scores are below 200, we need to run the MCMC chain for longer (or start another independent run). The ESS scores are shown for each parameter on the left hand side

```
Question 1: Are the ESS scores all over 200? Do they suggest we can use this log file for analysis?
```

We'll use previous BEAST runs (full details about the models and priors are in the 'Model setup' at the bottom of the tutorial) and first analyse log files which record the estimates of each parameter during the MCMC chain
