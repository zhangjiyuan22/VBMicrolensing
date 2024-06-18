# VBMicrolensing
`VBMicrolensing` is a tool for efficient computation in gravitational 
microlensing events using the advanced contour integration method, supporting single, binary and multiple lenses. 

In particular, VBMicrolensing is designed for the following calculations:
- **Magnification** by single, binary and multiple lenses
- **Centroid** of the images generated by single, binary and multiple lenses
- **Critical curves and caustics** of binary and multiple lenses
- Complete **light curves** including several higher order effects: limb darkening of the source, binary source, parallax, xallarap, circular and elliptic orbital motion.

The code has been developed by Valerio Bozza, University of Salerno, and collaborators.
It is written as a C++ library and wrapped as a Python package, the user can call the code from either C++ or Python.



## Documentation
Full [documentation for the use of VBmicrolensing in C++](/docs/C++/readme.md) ond p is available. This can be a good reference also for Python users. 

Furthermore, the vast majority of functions are documented with Python docstrings which can be accessed as, for example, `?VBBL.BinaryMag2()` in
a Jupyter notebook.

Note that the python wrapper does not support the user-defined limb-darkening law.

## License
VBMicrolensing is freely available to the community under the 
GNU Lesser General Public License Version 3 included in this repository.