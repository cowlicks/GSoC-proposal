## Student Information

Name: Blake Griffith

Email: Blake.a.griffith@gmail.com

Telephone: (713) 702-1366

IRC: cowlicks@irc.freenode.net. I'm in #scipy.

I do my version control as [cowlicks on GitHub](https://github.com/cowlicks)

[Twitter](https://twitter.com/cwlcks)

[Blog / homepage](http://cwl.cx)

### About me
I've been programming using the SciPy/Numpy for around 3 years for reasearch and homework assingnments and have always wanted 

previous work with SciPy:
* [Improvements to the multiply method in scipy.sparse](https://github.com/scipy/scipy/pull/516)
* [My proposed specification for boolean data type handling](https://github.com/cowlicks/scipy-sparse-boolean-spec)

[CV](cwl.cx/cv.pdf)

## University Information

University: The University of Texas at Austin

Major: double major math and physics

Current Year and Expected Graduation date: Senior, graduating December of 2013

Degree: I'll be graduating with two degrees, B.S. Math and Physics

## Improving the Sparse Matrix package in Scipy

The project has three main parts:  adding support for the bool dtype, improve interaction with numpy and python types, and adding features which numpy ndarray and matrices have. 

Adding bool support will start with writing a specification, then implementing it along with a test suite. Currently sparse matrices behave irratically when `dtype=bool`, this will adress that (see [issue #1533](http://projects.scipy.org/scipy/ticket/1533). Sparse matrices also have unexpected results with boolean operators. When two sparse matrices are compared a single True or False is returned, this is inconsistent with the way NumPy arrays are compared. 

Next, attention will turn to Sparse Matrices interactions with other python/numpy types. Again a specification will be drafted, then implemented along with a test suite. [Issue #1042](http://projects.scipy.org/scipy/ticket/1533) is an example of how NumPy's universal functions just don't work with the sparse matrices *TODO add link to failing tests*. Fixing this will probably require a patch to NumPy to do better checking for sparse types, as well as modifications to base classes in sparse matrices. There are also issues with sparse matrices and python types *TODO*

Finally when Sparse Matrices are playing nice with numpy and python types. Sparse features will be added which ndarrays have but sparse matrices do not. Like calling `.min()` or `.max()` along a give axis and multi dimensional indexing . Priority will first be given to the Compressed Sparse Row (csr) and Compressed Sparse Column (csc) types then Lists of Lists (lil) then all other types. The goal is functional parity with numpy's ndarrays and matrix objects. There are 

### Motivation
The Sparse package of Scipy is used extensively by other packages such as [Scikit-Learn](http://scikit-learn.org/stable/), and is integrated with [SymPy](), [Sage](), and [Numpy](), but a quick search of [Stackoverflow](http://stackoverflow.com/search?tab=newest&q=[scipy]%20sparse) or the scipy issues page will demonstrate that it needs work, and that there are several feature users would like.


### Timeline

I've broken the 3 pieces of my proposal up into 3 equally size blocks of time +/- one week, and have shifted the Coding period to start on May 27th and end on August 29th (with the consent of my mentor).

#### Pre application. Up to May 3rd.
* Familiarizing myself with scipy.sparse by investigating bug reports, reading documentation, 
* Building rapport with the Scipy community and my mentor.
* Writing this document.

#### Pre-official start. May 3rd - May27.
* Get a head start (my last day of school is May 3rd.)
* Query the community for feedback in regards to bool handling specification, numpy/python type handling specification, and additional features they would like to see in sparse.
* Submit my proposal for bool handling specification to the community. Get feedback, alter as needed until some consensus is reached.
* Write numpy type parity specification. How should numpy objects be handled by sparse functions? How should Sparse matrices be handled by Numpy functions? What can and cannot be expected to be on par for sparse matirices? What should just be done as spmatrix.toarray().numpymethod()? What sparse methods should return sparse matrices?

#### Monday May 27th -- Start bool handling
*Begin implementing bool operations portion of the specification in sparsetools/\*.h .
* Implement bool type handling part of the specification.
* Write tests for bool specification.

#### Week of June 17th -- Wrap up bool handling.
* All unit tests passing
* Code committed
* Documentation complete

#### Monday June 24th -- Start type handling!

#### Week of July 15th -- Wrap up type handling
* Wrap up type handling

#### Week of July 22nd -- new methods, features etc.
* Add ability to call .min() and .max() along an axis.

#### July 29th -- Submit mid-term evaluation! 
* At this point, I expect to have:
    * Implemented boolean specification, along with tests and documentation.
    * Fixed the interactions with NumPy universal functions to behave according to the specification, along with assosciated tests and documentation.
    * started features.

#### Week of August 26th -- Wrap up new features!
* My school begins on August 29th, so I'll cut work to around 1/3 to 1/4 of before
* Continue with features, bugs etc for the remaining weeks. slow pace.
* Week of September 2nd
* Week of September 9th
* September 23rd -- Final evaluation!

* Bonus points!
    * Specify how to add new sparse matrix types to the existing zoo.
#### Onward -- After Sept 16th
Use my now vast knowledge of Scipy to be a productive member of the community, maybe one day even receiving the honor of commit rights.

#### TODO add to timeline
* axis arguments, min(), max(). Like ndarray.max() .min()?
* multidimensional array indexing 
* Represent the LU factorization obtained via SuperLU as actual sparse matrices rather than in SuperLU's internal format.
* 64 bit indices.
* numpy type handling.
    * specify numpy type handling.
>  This would involve implementation of a dispatch mechanism where
>    np.multiply knows that it shouldn't try to do things itself and get
>    it wrong, but use e.g. csc\_matrix.multiply
    * handling of sparse matrices by numpy universal functions.
    * details of these numpy functions.


* performance improvements
* bool spec, spec with how other types should be handled.
* return different types
* testing suite


* numpy types handling 
* returning numpy types
    * mat mult with numpy type
    * comparison with numpy type
* returning sparse matrices
    * operations with scalars
    * operations with vector types
    * operations with matrix type
    

