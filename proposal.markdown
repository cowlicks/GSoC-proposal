#Improvements to the sparse package of Scipy: support for bool dtype and better interaction with NumPy

##Abstract
This proposal has two parts:

1. Add support for bool dtype to sparse matrices, as well as boolean operations so that sparse matrices behave more like NumPy ndarrays.  

Currently, sparse matrices cannot support boolean operations

2. Improve interaction of sparse matrix objects and other types. Especially NumPy ndarray objects and ufuncs. This will allow use of numpy.dot, .multiply, etc. making generic sparse and dense matrix code much easier to write. This will also involve adding new functions/methods (similar to numpy ufuncs) to the sparse package which will improve it's usabilty.

Both of these will be implemented according to separate specifications (written with community input), and testing suites.

## Student Information
Name: Blake Griffith  
IRC: cowlicks@irc.freenode.net. I'm in #scipy.  
I do my version control as [cowlicks on GitHub](https://github.com/cowlicks)  
[Twitter](https://twitter.com/cwlcks)  
[Blog / homepage](http://cwl.cx)  

### About me
I've been programming using the SciPy/Numpy for around 3 years for reasearch and homework assingnments and have always wanted to give back.
previous work with SciPy:
* [Improvements to the multiply method in scipy.sparse](https://github.com/scipy/scipy/pull/516)

There are a lot of projects on [my GitHub](https://github.com/cowlicks), many incomplete, here are a select few:
* [Townes profile solution](https://github.com/cowlicks/Townes_profile).
* [some data analysis scripts](https://github.com/cowlicks/2dnls-scripts/tree/master/analysis)

[CV](https://github.com/cowlicks/CV/raw/master/curriculum_vitae.pdf)

## University Information
University: The University of Texas at Austin  
Major: double major math and physics  
Current Year and Expected Graduation date: Senior, graduating December of 2013  
Degree: two degrees, B.S. Math and Physics  


# Timeline
I've shifted the Coding period to start on May 27th (with the consent of my mentor) and end earlier so I can return to school.

#### Before May 27th.
* Familiarizing myself with scipy.sparse by investigating bug reports, reading documentation, etc.
* Building rapport with the Scipy community and my mentor by trying to be helpful in #scipy and on the mailing list.
* Get a head start! (my last day of school is May 3rd.)
* Get community feedback on bool handling specification and ndarray handling specification. Write said specifications. (I've already started this.)

#### bool handling -- May 27th to July 8th (6 weeks)
In order:
* Implement suport for bool datatype (2 weeks)
* code review and unit tests (1 week)
* Implement boolean operations (2 weeks)
* code review and unit tests (1 week)
* Reduce this to 5 weeks?

#### NumPy interactions -- July 8th to August 26th (7 weeks)
In order:
* Modify NumPy universal functions (`ufuncs`) to be aware of sparse matrix types. (2 weeks)
* ??? Add a week or more specifically for consolidating pieces of the sparse interface, although consolidation is assumed in the adding ufunc functions. (1 week)
* Add sparse matrix functions(or methods) to handle calls from `ufuncs` (5 weeks)
    * `ufuncs` that should just operate on the dense form of the sparse matrix.    
    * Add C++ code for row-wise or column-wise broadcasting.
    * Implement sparse forms of the binary ufuncs that should broadcast. 
    * Test suite for all the sparse matrix methods which correspond to ufuncs.
* Mid-term evaluation, July 29th -- deliverables are:
    * bool spec implemented
    * Have at least one sparse matrix method that a NumPy ufunc will dispatch to.
* Wrap up. test suite for Numpy ufunc and sparse matrix interactions for sparse/dense and sparse/sparse combinations. (1 week)

#### Onward -- post August 27th
My school begins on August 29th, so I'll cut work to around 1/3 to 1/4 of before. So I will continue with a few features, and fixing bugs etc for the remaining weeks at a slow pace.  
Final evaluation, Sept 23rd -- deliverables are:
* bool spec implemented, along with documentation and test suite. 
    * support for bool dtype
    * support for boolean operations
* NumPy interaction spec implemented.
    * Many Numpy ufuncs work with sparse matricies, and sparse dense combinations. 
    * New and improved functions/methods in the sparse package (add, dot, divide, multiply, etc.)
    * A nicer interface and codebase with less repeated code. 

When all this is done I will use my now vast knowledge of Scipy to be a productive member of the community :)

#### bonus
Things I would like to try to fit in somewhere. Roughly in order of preference.
* axis arguments for min(), max().
* multidimensional array indexing 
* performance improvements
* Write spec for how to add new sparse matrix types to the existing zoo.
* Represent the LU factorization obtained via SuperLU as actual sparse matrices rather than in SuperLU's internal format.
* 64 bit indices.
