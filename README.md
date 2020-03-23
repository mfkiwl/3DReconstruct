# BADSLAM setup instructions on leonhard

## Ssh into leonhard
```
$ ssh <username>@login.leonhard.ethz.ch
```
## Clone repositories (yes you need to build badslam :/ )
```
$ git clone https://github.com/panpan2/3DReconstruct
$ git clone https://github.com/ETH3D/badslam
```

## Load cmake dependencies
```
$ module load new gcc/4.8.2 cmake/3.11.4
```

## Build instructions for linux
```
$ cd badslam
$ mkdir build_RelWithDebInfo
$ cd build_RelWithDebInfo
$ cmake -DCMAKE_BUILD_TYPE=RelWithDebInfo -DCMAKE_CUDA_FLAGS="-arch=sm_61" ..
$ make -j badslam  # Reduce the number of threads if running out of memory, e.g., -j3
```
If something doesn't seem to work make sure you have the dependencies of the REAMDE.md in badlsam

