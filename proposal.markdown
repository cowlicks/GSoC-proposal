#Improvements to the sparse package of Scipy: support for bool dtype and better interaction with NumPy

##Abstract
The scipy sparse package is used extensively in other projects like scikit-learn, and is integrated with NumPy, SymPy, and Sage.
However it leaves a lot to be desired. There is no support for boolean sparse matrices, and boolean operations on sparse matrices return inconsistent results. See [these]( http://projects.scipy.org/scipy/ticket/1533) [examples](http://projects.scipy.org/scipy/ticket/991). The sparse matrices also have problems when used with NumPy ufuncs and ndarrays (see this ticket which I did some work on, and [these](http://projects.scipy.org/scipy/ticket/1598)). The second part of this proposal is to remedy this. So writing code combining sparse dense matrices will be easier, and making the sparse codebase easier to maintain.

1. Add support for bool dtype to sparse matrices, as well as boolean operations so that sparse matrices behave more like NumPy ndarrays.  

2. Improve interaction of sparse matrix objects and other types. Especially NumPy ndarray objects and ufuncs. This will make numpy.dot, .multiply, etc. work with sparse matrices, making generic sparse and dense matrix code much easier to write. This will also involve adding new functions/methods (similar to numpy ufuncs) to the sparse package which will improve it's usabilty.

Both of these will be implemented according to separate specifications (written with community input), and testing suites.

## Student Information
Name: Blake Griffith  
email: [blake.a.griffith@gmail.com](mailto:blake.a.griffith@gmail.com)  
phone: (713) 702-1366  
IRC: [cowlicks@irc.freenode.net](mailto:cowlicks@irc.freenode.net). I'm in #scipy.  
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

#### bool handling -- May 27th to July 1st (5 weeks)
Implementation will be done according to this [specification](https://github.com/cowlicks/scipy-sparse-boolean-spec/blob/master/scipep.rst)
which is currently being written. In order:
* implement suport for bool datatype (2 weeks)
* implement boolean operations (2 weeks)
* code review and unit tests (1 week)

#### NumPy interactions -- July 1st to August 26th (8 weeks)
In order:
* Modify NumPy universal function objects (`ufuncs`) to be aware of sparse matrix types. (1 week)
* Refactor and consolidate sparse code to clean up the interface (1 week)
* Add sparse matrix functions(or methods) to handle calls from `ufuncs` (5 weeks)
    * Implement `ufuncs` that should just operate on the dense form of the sparse matrix.    
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
    * Support for bool dtype.
    * Support for boolean operations.
* NumPy interaction spec implemented.
    * Many Numpy ufuncs work with sparse matricies, and sparse dense combinations. Making sparse/dense code easier to write.
    * A nicer interface and codebase with less repeated code, more maintainable.

When all this is done I will use my now vast knowledge of Scipy to be a productive member of the community :)
