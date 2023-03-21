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

<img src="_figures/tracer_loaded.png", width = "500">

We'll use previous BEAST runs (full details about the models and priors are in the 'Model setup' at the bottom of the tutorial) and first analyse log files which record the estimates of each parameter during the MCMC chain
