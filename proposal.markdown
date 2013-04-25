## Student Information

Name: Blake Griffith

Email: Blake.a.griffith@gmail.com

Telephone: (713) 702-1366

IRC: cowlicks@irc.freenode.net. I'm in #scipy.

I do my version control as [cowlicks on GitHub](https://github.com/cowlicks)

[Twitter](https://twitter.com/cwlcks)

[Blog / homepage](http://cwl.cx)

## University Information

University: The University of Texas at Austin

Major: double major math and physics

Current Year and Expected Graduation date: Senior, graduating December of 2013

Degree: I'll be graduating with two degrees, B.S. Math and Physics

## Improving the Sparse Matrix package in Scipy
### Abstract

The project has three main parts, adding support for the bool dtype, having better interaction with numpy and python types, and adding features which numpy ndarray and matrices have. 

Adding bool support will start with writing a specification, implementing it along with a test suite. 

Next, attention will turn to Sparse Matrices interactions with other python/numpy types. Again a specification will be drafted, then implemented along with a test suite. 

Finally when Sparse Matrices are playing nice with numpy and python types. Spares features will be added to achieve parity with numpy types. Priority will first be given to the Compressed Sparse Row (csr) and Compressed Sparse Column (csc) types then Lists of Lists (lil) then all other types. The goal is functional parity with numpy's ndarrays and matrix objects.

### Motivation
The Sparse package of Scipy is used in several other packages, and a quick search of [Stackoverflow](http://stackoverflow.com/search?tab=newest&q=[scipy]%20sparse) will demonstrate that it needs work, and that there are several feature users would like.

### Timeline

#### Pre application. Up to May 3rd.
* Familiarizing myself with scipy.sparse by investigating bug reports, reading documentation, 
* Building rapport with the Scipy community and my mentor.
* Writing this document.

#### Pre official start. May 3rd - May27.
* Get a head start (my last day of school is May 3rd.)
* Submit my proposal for bool handling specification to the community. Get feedback, alter as needed until some consensus is reached.
* Write numpy type parity specification. How should numpy objects be handled by sparse functions? How should Sparse matrices be handled by Numpy functions? What can and cannot be expected to be on par for sparse matirices? What should just be done as spmatrix.toarray().numpymethod()? What sparse methods should return sparse matrices?

#### Weekly timeline May 27th
(I will probably start writing code before the *official start*)
* Week of May 27th
    * Begin implementing bool operations portion of the specification in sparsetools/\*.h .
    * Implement bool type handling part of the specification.
    * Write tests for bool specification.
* Week of June 3rd
    * Continue work on implementing bool spec.
    * Get all the tests passing.
* Week of June 10th
    * 
* Week of June 17th
* Week of June 24th
* Week of July 1st
* Week of July 8th
* Week of July 15th
* Week of July 22nd
* Week of July 29th
    * Submit mid-term evaluation! 
* Week of August 5th
* Week of August 12th
* Week of August 19th
* Week of August 26th
    * My school begins on August 29th, so I'll cut work to around 1/3 to 1/4 of before
* Week of September 2nd
* Week of September 9th
* Week of September 16th
    * Pencils Down!
* Bonus points
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
    

### Additional info about myself
Short paragraph, like would be on a cover letter.

previous work with SciPy:
* [Improvements to the multiply method in scipy.sparse](https://github.com/scipy/scipy/pull/516)
* [My proposed specification for boolean data type handling](https://github.com/cowlicks/scipy-sparse-boolean-spec)

Link to CV
