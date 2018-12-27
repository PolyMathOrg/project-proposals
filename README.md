# PolyMath Ideas List

This is the list of projects related to mathematics, numeric computation, statistics, data science, or machine learning that we wish to see implemented and integrated with [PolyMath](https://github.com/PolyMathOrg/PolyMath) or used together with it. Some of these projects will be proposed for [Google Summer of Code 2019](https://developers.google.com/open-source/gsoc/timeline). If you have any ideas - feel free to add them to the list. If you are a student who wants to take on a project from this list and need assistance, please contact us on #polymath channel of [Pharo Discord](https://pharo.org/community) or writing a letter to [PolyMath mailing list](http://groups.google.com/group/polymath-project).

## Contents
- [Native vector-matrix algebra](#native-vector-matrix-algebra)
- [DataFrame](#dataframe)
- [NLP library](#nlp-library)
- [Data visualizations](#data-visualizations)
- [Keras-style API on top of TensorFlow](#keras-style-api-on-top-of-tensorflow)
- [PolyMath examples](#polymath-examples)
- [Support for Vega visualization engine](#support-for-vega-visualization-engine)
- [Improve ODE-solver](#improve-ode-solver)
- [Rule-based integration](#rule-based-integration)
- [Computational algebra](#computational-algebra)

## Native vector-matrix algebra

Build a numeric library for matrix and vector algebra (similar to [PolyMath](https://github.com/PolyMathOrg/PolyMath) but smaller) with external backend such as  [BLAS](http://www.netlib.org/blas/), [LAPACK](http://www.netlib.org/lapack/), or [Intel MKL](https://software.intel.com/en-us/mkl). These are native libraries written in Fortran or C that provide routines for fast vector and matrix operations. All widely used numeric libraries and languages such as [numpy](http://www.numpy.org/), [R](https://www.r-project.org/), [Matlab](https://www.mathworks.com/products/matlab.html) make calls to these routines. PolyMath on the other hand has everything implemented in Smalltalk, which has many advantages, but it is so slow that in practice it's impossible to use PolyMath vector-matrix operations for most real applications (for example, in machine learning). There is an [existing library](http://www.squeaksource.com/Smallapack.html) for Squeak to use LAPACK.

## DataFrame

[PolyMath DataFrame](https://github.com/PolyMathOrg/DataFrame) is a Smalltalk library similar to [pandas](https://pandas.pydata.org/) in Python or [data.frames](https://www.rdocumentation.org/packages/base/versions/3.5.1/topics/data.frame) in R. It implements data structures for processing and analysing tabular data which is an essential part of data science and machine learning workflow. DataFrame needs a lot of improvement, both fixing the existing features and adding new ones.

## NLP library

We need a natural language processing (NLP) library entirely written in Pharo with functionality similar to [NLTK](https://www.nltk.org/) or [Spacy](https://spacy.io/): [part of speech (PoS) tagging](https://en.wikipedia.org/wiki/Part-of-speech_tagging), [named entity recognition (NER)](https://en.wikipedia.org/wiki/Named-entity_recognition), [lemmatization](https://en.wikipedia.org/wiki/Lemmatisation), [stemming](https://en.wikipedia.org/wiki/Stemming), [word sense disambiguation](https://en.wikipedia.org/wiki/Word-sense_disambiguation), [tf-idf](https://en.wikipedia.org/wiki/Tf%E2%80%93idf), [n-grams](https://en.wikipedia.org/wiki/N-gram), various metrics etc. There is an [existing NLP library](https://github.com/mark-watson/nlp_smalltalk) that implements part of the mentioned features.

## Data visualizations

We need a simple and powerful data visualization (charting) library similar to [ggplot](https://ggplot2.tidyverse.org/) and based on [The Grammar of Graphics](https://www.amazon.com/Grammar-Graphics-Statistics-Computing/dp/0387245448/ref=as_li_ss_tl?ie=UTF8&qid=1477928463&sr=8-1&keywords=the+grammar+of+graphics&linkCode=sl1&tag=ggplot2-20&linkId=f0130e557161b83fbe97ba0e9175c431). Inspiration can also be taken from Python's [matplotlib](https://matplotlib.org/) and [seaborn](https://seaborn.pydata.org/) but they do not follow the Grammar (which is very preferable). The library must be entirely implemented in Pharo, elements of visualization must be objects that allow interaction and can be inspected. This can be done by using [Telescope's Geometry library](https://github.com/TelescopeSt/Geometry) as back-end. Existing libraries for data visualization in Pharo include [Roassal's charting functionalities](http://agilevisualization.com/AgileVisualization/Grapher/0203-Grapher.html) and [a bridge to Python's matplotlib](https://github.com/juliendelplanque/MatplotLibBridge), however none of them fully satisfies the conditions listed above.

## Keras-style API on top of TensorFlow

[PolyMathOrg](https://github.com/PolyMathOrg/libtensorflow-pharo-bindings) provides bindings to use [TensorFlow](https://www.tensorflow.org/) inside [Pharo](https://pharo.org/). We need to design a high-level API similar to [Keras](https://keras.io/) that would be easy to work with and allow fast experimentation. There is an [existing bridge](https://github.com/ObjectProfile/KerasWrapper) that calls Keras functions from Python. We need to have similar API with [Pharo TensorFlow](https://github.com/PolyMathOrg/libtensorflow-pharo-bindings) as a backend.

## PolyMath examples

More PolyMath examples, have more integration with [Roassal](http://agilevisualization.com/) and/or [GToolkit](https://github.com/feenkcom/gtoolkit).

## Support for Vega visualization engine

Add support for [Vega visualization engine](https://vega.github.io/vega/).

## Improve ODE-solver

PolyMath has [a simple ODE-solver](https://github.com/PolyMathOrg/PolyMath/tree/development/src/Math-ODE). We would like to have more elaborate ways of solving ODE like [the ones in Julia](https://openresearchsoftware.metajnl.com/articles/10.5334/jors.151/).

## Rule-based integration

Implement rule-based integration such as [Rubi](https://rulebasedintegration.org/).

## Computational algebra

Add support for [GAP - Groups, Algorithms, Programming - a System for Computational Discrete Algebra computational algebra](https://www.gap-system.org/). There is an [existing implementation](https://github.com/len/Mathematics) in Cuis Smalltalk.
