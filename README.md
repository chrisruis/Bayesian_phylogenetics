# Examining substitution rates and ancestor dates with BEAST
Materials for Bayesian phylogenetics tutorial

This tutorial requires prior installation of Tracer (downloaded from https://github.com/beast-dev/tracer/releases) and FigTree (downloaded from https://github.com/rambaut/figtree/releases)

In this tutorial, we will analyse the output from BEAST analyses of two pandemic variants of norovirus, a highly prevalent cause of gastroenteritis. We aim to:
1) Identify the substitution rate of each variant
2) Compare the substitution rates between variants
3) Examine ancestor dates to make inferences about the drivers of pandemic spread

We'll use previous BEAST runs (full details about the models and priors are in the 'Model setup' at the bottom of the tutorial) and first analyse log files which record the estimates of each parameter during the MCMC chain
