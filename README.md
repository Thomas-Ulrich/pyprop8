[![DOI](https://joss.theoj.org/papers/10.21105/joss.04217/status.svg)](https://doi.org/10.21105/joss.04217) [![PyPI version](https://badge.fury.io/py/pyprop8.svg)](https://badge.fury.io/py/pyprop8) [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/valentineap/pyprop8/HEAD?labpath=examples%2Fdemo.ipynb)

# pyprop8

This package provides a lightweight Python implementation of the seismogram calculation algorithm set out in [O'Toole & Woodhouse (2011)](https://doi.org/10.1111/j.1365-246X.2011.05210.x), together with the source derivatives set out in [O'Toole, Valentine & Woodhouse (2012)](https://doi.org/10.1111/j.1365-246X.2012.05608.x). It is intended to provide a lightweight, easy-to-install seismological forward model suitable for use in teaching and research (in particular, to provide a computationally-cheap yet physically-realistic forward problem for use in the development and testing of inversion algorithms).

Full documentation is [available here](https://pyprop8.readthedocs.io/), and you can try the package out [using Binder](https://mybinder.org/v2/gh/valentineap/pyprop8/HEAD?labpath=examples%2Fdemo.ipynb).

A list of projects that have made use of `pyprop8` can be found [here](USERS.md); please feel free to [add your own](CONTRIBUTING.md).

## Installation

The easiest way to get this package is through `pip`, e.g.
```
pip install pyprop8
```
Alternatively, you can clone this repository and ensure that the contents of the `src/` directory are placed somewhere where they can be found by your Python installation, e.g. by setting the $PYTHONPATH environment variable.

## Dependencies

The core functions of this package depend only on:
- [numpy](https://numpy.org)
- [scipy](https://scipy.org)

`pyprop8` will also use [`tqdm`](https://github.com/tqdm/tqdm) if it is available, to display progress bars. 

Some of the examples found in `examples/` may have additional dependencies and requirements, including [Jupyter](https://jupyter.org) and [`matplotlib`](https://matplotlib.org'). Look for a `requirements.txt` file in the relevant example directory; you can install the necessary pacakges using the command `pip install -r requirements.txt`.

## Citing this package

If you make use of this code, please acknowledge the work that went into developing it! In particular, if you are preparing a publication, we would appreciate it if you cite both the paper describing the general method, and this specific implementation:

- [O'Toole, T.B. & J.H. Woodhouse (2011)](https://doi.org/10.1111/j.1365-246X.2011.05210.x), "Numerically stable computation of complete synthetic seismograms including the static displacement in plane layered media", Geophysical Journal International, 187, pp.1516-1536, doi:10.1111/j.1365-246X.2011.05210.x
- [Valentine, A.P. & M. Sambridge (2022)](https://doi.org/10.21105/joss.04217), "`pyprop8`: A lightweight code to simulate seismic observables in a layered half-space", Journal of Open Source Software, 7, 4217, doi:10.21105/joss.04217.


If your work relies on being able to calculate the source parameter derivatives, you should also cite the paper describing how these are obtained:

- [O'Toole, Valentine & Woodhouse (2012)](https://doi.org/10.1111/j.1365-246X.2012.05608.x), "Centroid–moment tensor inversions using high-rate GPS waveforms", Geophysical Journal International, 191, pp.257-270, doi:10.1111/j.1365-246X.2012.05608.x.

## Acknowledgements

This package was developed at the Australian National University and Durham University by Andrew Valentine. It builds on earlier work by Tom O'Toole and John Woodhouse, and has benefited from sight of code written by those authors. In particular, the exponential rescaling of the propagator matrices is inspired by their implementation. However, the present code has been developed 'from scratch' based on the published algorithms.

This work has received support from the Australian Research Council under grants DE180100040 and DP200100053.
