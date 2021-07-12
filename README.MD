This repo is a fork of Warren Weckeser's 'eyediagram' repo [https://github.com/WarrenWeckesser/eyediagram].

Basically, it is just an updated version of his code (for instance, scipy's API has changed, and the function 'set_bg_color' - used in the original code - does not work anymore) with some small improvements and added functionality.

To build and install the package it is necessary to have cython and scipy installed. A common error when building the package is 'unable to find vcvarsall.bat'. You need to install the necessary Windows Compiler tools. For python 3.5 and later, you can install the latest version of Visual Studio and make sure that you include the "Python development workload" when selection what to install https://devblogs.microsoft.com/python/unable-to-find-vcvarsall-bat/]. 

I reproduce here verbatim Warren Weckeser's original README file:

'eyediagram' is a python library for generating eye diagrams (also known as eye patterns [http://en.wikipedia.org/wiki/Eye_pattern]).

This is prototype-quality software. The documentation is thin, and the API may change.

To build the package, cython and numpy must be installed.

To use the package, numpy and scipy must be installed. Plots are generated with either matplotlib (http://matplotlib.org/) or bokeh (http://bokeh.pydata.org/), so usually either one of those must be installed. However, the core function eyediagram.core.grid_count generates a numpy array that can be displayed or saved as an image using any other plotting or image-handling software, so it is not a strict requirement that matplotlib or bokeh be installed. See the example pyqtgraph_demo.py below for an example that uses pyqtgraph (http://www.pyqtgraph.org/) to display the eye diagram. Another example, chaco_demo.py in the demo directory of the source code, uses chaco (https://github.com/enthought/chaco) to plot the eye diagram.