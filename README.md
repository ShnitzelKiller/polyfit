# PolyFit: Clip-art vectorization
Code & Data for the SIGGRAPH 2020 paper [PolyFit: Perception-Aligned Vectorization of Raster Clip-art via Intermediate Polygonal Fitting](http://www.cs.ubc.ca/labs/imager/tr/2020/ClipArtVectorization/)

## Building
`git clone --recursive https://github.com/dedoardo/polyfit`

Open the folder or CMake generated solution in Visual Studio (use a 2017 compiler) and build polyfit.exe in Release(WithDebInfo) mode, the output will be written to the cmake source directory.

## Running
`polyfit.exe "data/binary_input/pear-32/input.png" "trained/random_forest_paper.txt" vectorization`

The output will be written to `vectorization/curves_closed.svg`

If you are interested in visualizing different stages of the algorithm, uncomment the respective lines in `apps/polyfit.cpp` and rebuild.

## Data
All the results shown in the paper and used in the user study are contained in the data directory.

## Dependencies
The code depends on the following libraries, but they should be handled automatically through git submodule.
- [Eigen 3.3+](http://eigen.tuxfamily.org/index.php?title=Main_Page)
- [Andre's Random Forest](https://github.com/bjoern-andres/random-forest)
- [Cairo](https://cairographics.org/download/)
- [Sean Barret's stb](https://github.com/nothings/stb)

## Some of the known problems
- Complex pixel-art will likely not work as the multicolor code hasn't been tested on it.
- Visual Studio 2019 *might* not work, we encountered some problems with incorrect variable initialization.

## TODOs
- Add instructions for training data
- Debug pixel-art

## Contact
Feel free to reach out at edoaramis at gmail.com for questions regarding the code. 
