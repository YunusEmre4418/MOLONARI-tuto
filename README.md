# MOLONARI-tuto

Tutorials for MOLONARI-computo: generating synthetic data with the direct model of pyheatmy, and estimating the
parameters of the river bed from them with the MCMC of bayesian_inversion.

- `01_generate_data.ipynb`: generates the synthetic data set `.data/Synthetic01` and its true parameters
  (`truth.json`); it needs pyheatmy only.
- `02_inversion.ipynb`: Bayesian inversion of this data set, compared with the true parameters at the end; it
  needs pyheatmy and bayesian_inversion.

They run in the environment of the MOLONARI-computo tree, which installs both packages from `sources/`:
`pixi install` at the root of the tree, then the Python of `.pixi/envs/default` as the kernel.
