# MOLONARI-tuto

Tutorials for MOLONARI-computo: generating synthetic data with the direct model of pyheatmy, and estimating the
parameters of the river bed from them with the MCMC of bayesian_inversion.

- `01_generate_data.ipynb`: generates the synthetic data set `.data/Synthetic01` and its true parameters
  (`truth.json`); it needs pyheatmy only.
- `02_inversion.ipynb`: Bayesian inversion of this data set, compared with the true parameters at the end; it
  needs pyheatmy and bayesian_inversion. Its MCMC takes about four minutes.

The data set is committed, so that `02_inversion.ipynb` runs on its own; running `01_generate_data.ipynb` writes
the same files again, and is needed only when the direct model of pyheatmy changes.

They run in the environment of the MOLONARI-computo tree, which installs both packages from `sources/`:
`pixi install` at the root of the tree, then the Python of `.pixi/envs/default` as the kernel. They use the
interface of pyheatmy 0.12 and bayesian_inversion 0.4, the versions of the release MOLONARI-computo-2 of the tree.
