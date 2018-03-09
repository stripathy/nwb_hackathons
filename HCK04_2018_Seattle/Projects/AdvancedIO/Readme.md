Back to [Projects List](../../README.md#ProjectsList)

# Advanced Data I/O via PyNWB

## Key Investigators

- Oliver Ruebel (LBNL)
- Andrew Tritt (LBNL)
- Ben Dichter
- Thomas Braun
- Jean-Christophe Fillion-Robin (Kitware)
- Aaron D. Milstein  (Stanford)

# Project Description

Enhance and gather requirements for advanced data I/O features, e.g.:
  * Compression
  * Iterative data write
  * Data streaming
  * MPI parallel I/O

## Objective

1. Create list of requirments for the various advanced I/O features
1. Expand existing advanced I/O features as needed to better support the requirements
1. As approbriate, prioritize and define plan for how the features could be implemented

## Current functionality

1. Basic compression is currently supported via the [H5DataIO](http://pynwb.readthedocs.io/en/latest/pynwb.form.backends.hdf5.h5_utils.html#pynwb.form.backends.hdf5.h5_utils.H5DataIO) class. An example for how to use H5DataIO is part of the PyNWB docs http://pynwb.readthedocs.io/en/latest/example.html#compressing-datasets .
1. Iterative data write (and streaming) are currrently supported via:
  * [DataChunkIterator](http://pynwb.readthedocs.io/en/latest/pynwb.form.data_utils.html#pynwb.form.data_utils.DataChunkIterator) Class for defining and iterating over data chunks. A number of additional classes related to the iterative data write are defined in the [data_utils](pynwb.readthedocs.io/en/latest/pynwb.form.data_utils.html#pynwb.form.data_utils) module, e.g. [AbstractDataChunkInterator](pynwb.readthedocs.io/en/latest/pynwb.form.data_utils.html#pynwb.form.data_utils), [DataChunk](pynwb.readthedocs.io/en/latest/pynwb.form.data_utils.html#pynwb.form.data_utils), [ShapeValidator](pynwb.readthedocs.io/en/latest/pynwb.form.data_utils.html#pynwb.form.data_utils), etc.
  * [HDF5IO](http://pynwb.readthedocs.io/en/latest/pynwb.form.backends.hdf5.h5tools.html#pynwb.form.backends.hdf5.h5tools.HDF5IO) implements the actual iterative data write (see ``__chunked_iter_fill__`` function)
  * [monitoring](pynwb.readthedocs.io/en/latest/pynwb.form.monitor.html) 
  * A start for a tutorial for iterative data write is on the following branch but its far from complete: https://github.com/NeurodataWithoutBorders/pynwb/compare/iter_write_tutorial
  
## Approach and Plan

1. Review existing functionality in PyNWB for compression, iterative write, streaming, and parallel I/O
1. Identify missing features
1. Prioritize and define plan for implementing missing features and identify implementation leads for the different features. 

## Progress and Next Steps

<!--Describe progress and next steps in a few bullet points as you are making progress.-->

# Illustrations

<!--Add pictures and links to videos that demonstrate what has been accomplished.-->

<!--![Description of picture](Example2.jpg)-->

<!--![Some more images](Example2.jpg)-->

# Background and References

<!--Use this space for information that may help people better understand your project, like links to papers, source code, or data.-->

- Forum: https://github.com/orgs/NeurodataWithoutBorders/teams/YourSubTeam
- Source code: https://github.com/YourUser/YourRepository
- Documentation: https://link.to.docs
- Test data: https://link.to.test.data