# Mesh Zoo

[![Build Status](https://travis-ci.org/nschloe/meshzoo.svg?branch=master)](https://travis-ci.org/nschloe/meshzoo)
[![codecov](https://codecov.io/gh/nschloe/meshzoo/branch/master/graph/badge.svg)](https://codecov.io/gh/nschloe/meshzoo)
[![Code Health](https://landscape.io/github/nschloe/meshzoo/master/landscape.svg?style=flat)](https://landscape.io/github/nschloe/meshzoo/master)
[![PyPi Version](https://img.shields.io/pypi/v/meshzoo.svg)](https://pypi.python.org/pypi/`meshzoo)
[![PyPi Downloads](https://img.shields.io/pypi/dm/meshzoo.svg)](https://pypi.python.org/pypi/meshzoo)
[![GitHub stars](https://img.shields.io/github/stars/nschloe/meshzoo.svg?style=social&label=Star&maxAge=2592000)](https://github.com/nschloe/meshzoo)

Mesh Zoo provides a couple of simple example meshes that can be used for your
FEM/FVM application.

Example usage:
```python
points, cells = meshzoo.rectangle.create_mesh(
    edgelength=2.0,
    nx=101,
    zigzag=True
    )

# Process the mesh, e.g., write it to a file using meshio
# meshio.write('rectangle.e', points, {'triangle': cells})
```

In addition to this, the `examples/` directory contains a couple of instructive
examples for other mesh generators like

  * [MeshPy](https://github.com/inducer/meshpy),
  * [meshzoo](https://github.com/nschloe/meshzoo), and
  * [mshr](https://bitbucket.org/fenics-project/mshr).


### Showcase

![](https://nschloe.github.io/meshzoo/hexagon.png)
![](https://nschloe.github.io/meshzoo/pacman.png)
![](https://nschloe.github.io/meshzoo/moebius.png)
![](https://nschloe.github.io/meshzoo/tetrahedron.png)
![](https://nschloe.github.io/meshzoo/screw.png)
![](https://nschloe.github.io/meshzoo/toy.png)

### Installation

#### Python Package Index

meshzoo is [available from the Python Package
Index](https://pypi.python.org/pypi/meshzoo/), so to install/upgrade simply type
```
pip install meshzoo -U
```

#### Manual installation

Download meshzoo from [PyPi](https://pypi.python.org/pypi/meshzoo/)
or [GitHub](https://github.com/nschloe/meshzoo) and
install it with
```
python setup.py install
```

### Testing

To run the Mesh Zoo unit tests, check out this repository and run
```
nosetests
```
or
```
nose2 -s test
```


### Distribution

To create a new release

1. bump the `__version__` number,

2. create a Git tag,
    ```
    git tag v0.3.1
    git push --tags
    ```
    and

3. upload to PyPi:
    ```
    make upload
    ```


### License

Mesh Zoo is published under the [MIT license](https://en.wikipedia.org/wiki/MIT_License).
