# Rotate a grey-scale images by 45 degree. 

## Overview
This is a image tool that rotates a grey-scale image by 45 degree and output it a file. 
The image processing is fulfilled by the Nvidia NPP libraries. Npp libraries leverage GPUs to do actual rotation operation.

## Code Organization

```bin/```
This folder should hold all binary/executable code that is built automatically or manually. Executable code should have use the .exe extension or programming language-specific extension.

```data/```
This folder should hold all example data in any format. If the original data is rather large or can be brought in via scripts, this can be left blank in the respository, so that it doesn't require major downloads when all that is desired is the code/structure.

```lib/```
Any libraries that are not installed via the Operating System-specific package manager should be placed here, so that it is easier for inclusion/linking.

```src/```
The source code should be placed here in a hierarchical fashion, as appropriate.

```README.md```
This file should hold the description of the project so that anyone cloning or deciding if they want to clone this repository can understand its purpose to help with their decision.

```INSTALL```
This file should hold the human-readable set of instructions for installing the code so that it can be executed. If possible it should be organized around different operating systems, so that it can be done by as many people as possible with different constraints.

```Makefile or CMAkeLists.txt or build.sh```
There should be some rudimentary scripts for building your project's code in an automatic fashion.

```run.sh```
An optional script used to run your executable code, either with or without command-line arguments.
# CUDA.at.Scale.Independent.Project
Code project for CUDA at Scale Independent Project

## Tutorial on run it manually. 
```
coder@dcf28851ac5f:~/project/IndepProject/CUDA.at.Scale.Independent.Project/bin$ ./imageRotateNPP.exe --input ../data/Lena.pgm 
./imageRotateNPP.exe Starting...

MapSMtoCores for SM 8.9 is undefined.  Default to use 128 Cores/SM
MapSMtoArchName for SM 8.9 is undefined.  Default to use Ampere
GPU Device 0: "Ampere" with compute capability 8.9

NPP Library Version 11.3.3
  CUDA Driver  Version: 12.6
  CUDA Runtime Version: 11.3
MapSMtoArchName for SM 8.9 is undefined.  Default to use Ampere
  Device 0: <          Ampere >, Compute SM 8.9 detected
nppiRotate opened: <../data/Lena.pgm> successfully!
srcROI: x:0, y:0, width:512, height:512
aBoundingBox: [0.000000, -361.331565 | 722.663130, 361.331565]
destROI: x:0, y:0, width:722, height:722
ShiftX:0, shiftY:361.000000
Saved image: ../data/Lena_rotate.pgm
```
