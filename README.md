# VBMicrolensing
`VBMicrolensing` is a tool for efficient computation in gravitational 
microlensing events using the advanced contour integration method, supporting single, binary and multiple lenses. 

In particular, VBMicrolensing is designed for the following calculations:
- **Magnification** by single, binary and multiple lenses
- **Centroid** of the images generated by single and binary lenses
- **Critical curves and caustics** of binary and multiple lenses
- Complete **light curves** including several higher order effects: limb darkening of the source, binary source, parallax, xallarap, circular and elliptic orbital motion.

`VBMicrolensing` is written as a C++ library and wrapped as a Python package, the user can call the code from either C++ or Python. This new code encompasses the well-known [VBBinaryLensing](https://github.com/valboz/VBBinaryLensing) code, which is at the basis of several platforms for microlensing modeling. `VBBinaryLensing` will still be available as a legacy software, but will no longer be maintained. 

`VBMicrolensing` has been developed by **Valerio Bozza**, University of Salerno, with a substantial contribution by **Vito Saggese**, University of Naples. We also acknowledge a long list of collaborators who contributed to testing and development of particular aspects over the years: Etienne Bachelet, Fran Bartolic, Sebastiano Calchi Novati, Giovanni Covone, Giuseppe D'Ago, Tyler Heintz, Ava Hoag, Markus Hundertmark, Elahe Khalouei, Radek Poleski, Paolo Rota, Sedighe Sajadian, Rachel Street, Jiyuan Zhang, Keto Zhang, Weicheng Zhang, Wei Zhu.

## Attribution
Any use of this code for scientific publications should be acknowledged by a citation to the works relevant to your study:
- [V. Bozza, MNRAS 408 (2010) 2188](https://ui.adsabs.harvard.edu/abs/2010MNRAS.408.2188B/abstract): general algorithm for binary lensing;
- [V. Bozza et al., MNRAS 479 (2018) 5157](https://ui.adsabs.harvard.edu/abs/2018MNRAS.479.5157B/abstract): BinaryMag2 function, Extended-Source-Point-Lens methods; 
- [V. Bozza, E. Khalouei and E. Bachelet, MNRAS 505 (2021) 126](https://ui.adsabs.harvard.edu/abs/2021MNRAS.505..126B/abstract): astrometry, generalized limb darkening, Keplerian orbital motion; 
- V. Bozza, v. Saggese, G. Covone & P. Rota (2024), in preparation: multiple lenses.

If specifically relevant to your work, please also cite
[J. Skowron and A. Gould, arXiv:1203.1034](https://arxiv.org/abs/1203.1034).
 
## Installation

### Python

The easiest way to install `VBMicrolensing` is through `pip install VBMicrolensing`

In alternative, in order to use the latest build, clone this GitHub repository on your computer, enter your local copy of the repository and run
```
pip install .
```

Currently, `VBMicrolensing` works on Linux, Windows, MacOS and python >= 2.7. The package requires a C++ compiler supporting C++17.

### C++

If you just want to use the C++ library, clone this repository, all cpp files and the 
`VBMicrolensing.h` are located in in `VBMicrolensing/lib` and should be added to your project. 

The package also contains the following files:
- `VBMicrolensing/data/ESPL.tbl`  - Pre-calculated table for Extended-source-point-lens
- `VBMicrolensing/data/OB151212coords.txt` - Sample file with event coordinates
- `VBMicrolensing/data/satellite1.txt` - Sample table for satellite position (Spitzer)
- `VBMicrolensing/data/satellite2.txt` - Sample table for satellite position (Kepler)
  
## Documentation
Full [documentation for the use of VBmicrolensing in python](/docs/python/readme.md) and [documentation for the use of VBmicrolensing in C++](/docs/C++/readme.md) are available.

Furthermore, the vast majority of functions are documented with Python docstrings which can be accessed as, for example, `?VBBL.BinaryMag2()` in
a Jupyter notebook.

We also provide some [examples](examples) showing the capabilities of the package. In particular, we reproduce some known triple-lense microlensing events.

## License
VBMicrolensing is freely available to the community under the 
GNU Lesser General Public License Version 3 included in this repository.
