# CuML

This repo contains machine learning algorithms to be used with [PyGDF](https://github.com/gpuopenanalytics/pygdf). Current algorithms are:

1. Truncated Singular Value Decomposition (tSVD)
2. Principal Component Analysis (PCA)
3. Density-based spatial clustering of applications with noise (DBSCAN)

This repository contains the high level functionality of this algorithms, the ML primitives can be found in the ml-prims repo.

## Setup

To use CuML, it must be cloned and built in an environment that already where the dependencies, including PyGDF, libgdf and their own dependencies, are already installed.

### Dependencies

1. zlib
2. cmake (>= 3.8, version 3.11.4 is recommended and there are issues with version 3.12)
3. CUDA SDK (>= 8.0)
4. Cython (>= 0.28)
5. gcc (>=5.4.0)
6. nvcc
7. PyGDF

### Building CuML:

To install CuML from source, clone the repository and its submodules:

## Repo
```bash
$ git clone --recursive https://gitlab-master.nvidia.com/RAPIDS/cuML
```

To install CuML to be used from Python, in the root directory of the repository:

```
python setup.py install
```

### Running tests

To test the algorithms:

```bash
$ mkdir build
$ cd build
$ cmake ..
$ make -j
$ ./ml_test
```

### Python Tests

Additional python tests can be found in the pythontests folder, and contains some useful scripts. <!-- Refer to [scripts](scripts/README.md). -->

## External

The external folder contains submodules that this project in-turn depends on. Appropriate location flags
will be automatically populated in the main CMakeLists.txt file for these.

Current external submodules are:

- (CUTLASS)[https://github.com/NVIDIA/cutlass]
- (Google Test)[https://github.com/google/googletest]
- ml-prims

## Contributing

In progress.