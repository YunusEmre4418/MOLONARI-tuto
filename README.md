# MOLONARI-tuto

Tutorials for MOLONARI-computo: generating synthetic data with the direct model of pyheatmy, estimating the
parameters of the river bed from them with the MCMC of bayesian_inversion, and estimating them from the real data
of a monitoring point.

- `01_generate_data.ipynb`: generates the synthetic data set `.data/Synthetic01` and its true parameters
  (`truth.json`); it needs pyheatmy only.
- `02_inversion.ipynb`: Bayesian inversion of this data set, compared with the true parameters at the end; it
  needs pyheatmy and bayesian_inversion. Its MCMC takes about four minutes.
- `03_real_data.ipynb`: Bayesian inversion of the real data of the monitoring point Point034 (`.data/Point034`, a
  copy of `data/Point034_processed` of MOLONARI-computo), which have no true parameters to compare with; it needs
  pyheatmy and bayesian_inversion. Its MCMC takes about four minutes.

The data sets are committed, so that `02_inversion.ipynb` and `03_real_data.ipynb` run on their own; running
`01_generate_data.ipynb` writes the same synthetic files again, and is needed only when the direct model of pyheatmy
changes.

They run in the environment of the MOLONARI-computo tree, which installs both packages from `sources/`:
`pixi install` at the root of the tree, then the Python of `.pixi/envs/default` as the kernel. They use the
interface of pyheatmy 0.12 and bayesian_inversion 0.4, the versions of the release MOLONARI-computo-2 of the tree.
