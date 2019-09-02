complex_bessel
==============

This is a fork of https://github.com/joeydumont/complex_bessel

A C++ library to evaluate Bessel functions of all kinds. More information can 
be found on the [website](http://valandil.github.io/complex_bessel).

The CMakeLists.txt is modified in order to create a complex_bessel.lib and complex_bessel.dll for static dll implementation in windows visual studio.

## Compilation Instructions for windows visual studio users. 

### Step 1: The library uses CMake for compilation. Install Cmake for windows https://cmake.org/download/.

Download for example cmake-3.15.2-win64-x64.zip.

(Ninja generator 1.8.2 included in visual studio 2019 does not support Fortran)

### Step 2: In cmd command window run build.sh 

If it works, go to directly step 5.

If it doesn’t work, it creates at least build and out directories

Follow steps 3 and 4 to generate complex_bessel.lib and complex_bessel.dll manually 

### Step 3: Run cmake-gui.exe and configure to the visual studio version with the correct Fortran compiler. 

Set the source code repository, which contains CMakeLists.txt and the build repository (if it doesn’t exist, it will be created)

Configure: specify the generator for the visual studio version that contains Fortran compiler
![Cmake_configure](/tests/cmake_configure.png)

Generate and open Project with the corresponding visual studio version

### Step 4:	Generate with Release version in visual studio
The complex_bessel.lib and complex_bessel.dll are in Release file in build path
![compile-fortran](/tests/compile-fortran.png)

### Step 5:	configure visual studio for mixed-language applications

Follow steps in https://software.intel.com/en-us/articles/configuring-visual-studio-for-mixed-language-applications 
![configure_vs](/tests/configure_vs.png)

