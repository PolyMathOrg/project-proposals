# PolyMath Ideas List

This is the list of projects related to mathematics, numeric computation, statistics, data science, or machine learning that we wish to see implemented and integrated with [PolyMath](https://github.com/PolyMathOrg/PolyMath). Some of these projects will be proposed for [Google Summer of Code 2019](https://developers.google.com/open-source/gsoc/timeline). If you have any ideas - feel free to add them to the list. If you are a student who wants to take on a project from this list and need assistance, please contact us on #polymath channel of [Pharo Discord](https://pharo.org/community) or writing a letter to [PolyMath mailing list](http://groups.google.com/group/polymath-project).

## Contents
- [Native vector-matrix algebra](#native-vector-matrix-algebra)
- [DataFrame](#dataframe)

## Native vector-matrix algebra

Build a numeric library for matrix and vector algebra (similar to [PolyMath](https://github.com/PolyMathOrg/PolyMath) but smaller) with external backend such as  [BLAS](http://www.netlib.org/blas/), [LAPACK](http://www.netlib.org/lapack/), or [Intel MKL](https://software.intel.com/en-us/mkl). These are native libraries written in Fortran or C that provide routines for fast vector and matrix operations. All widely used numeric libraries and languages such as [numpy](http://www.numpy.org/), [R](https://www.r-project.org/), [Matlab](https://www.mathworks.com/products/matlab.html) make calls to these routines. PolyMath on the other hand has everything implemented in Smalltalk, which has many advantages, but it is so slow that in practice it's impossible to use PolyMath vector-matrix operations for most real applications (for example, in machine learning). There is an [existing library](http://www.squeaksource.com/Smallapack.html) for Squeak to use LAPACK.

## DataFrame

[PolyMath DataFrame](https://github.com/PolyMathOrg/DataFrame) is a Smalltalk library similar to [pandas](https://pandas.pydata.org/) in Python or [data.frames](https://www.rdocumentation.org/packages/base/versions/3.5.1/topics/data.frame) in R. It implements data structures for processing and analysing tabular data which is an essential part of data science and machine learning workflow. DataFrame needs a lot of improvement, both fixing the existing features and adding new ones.
