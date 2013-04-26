# Short description
This proposal has two parts:

1. Add support for bool dtype to sparse matrices, as well as boolean operations so that sparse matrices behave more like NumPy ndarrays.

2. Improve interaction of sparse matrix objects and other types. Especially NumPy ndarray objects and ufuncs.

Both of these will be implemented according to separate specifications (written with community input), and testing suites.

## Student Information
Name: Blake Griffith  
Email: Blake.a.griffith@gmail.com  
Telephone: (713) 702-1366  
IRC: cowlicks@irc.freenode.net. I'm in #scipy.  
I do my version control as [cowlicks on GitHub](https://github.com/cowlicks)  
[Twitter](https://twitter.com/cwlcks)  
[Blog / homepage](http://cwl.cx)  

### About me
I've been programming using the SciPy/Numpy for around 3 years for reasearch and homework assingnments and have always wanted to give back.
previous work with SciPy:
* [Improvements to the multiply method in scipy.sparse](https://github.com/scipy/scipy/pull/516)

There are a lot of projects on [my GitHub](https://github.com/cowlicks), many incomplete, here are a select few:
* Townes profile
* ??

[CV](cwl.cx/cv.pdf)

## University Information
University: The University of Texas at Austin  
Major: double major math and physics  
Current Year and Expected Graduation date: Senior, graduating December of 2013  
Degree: two degrees, B.S. Math and Physics  


# Timeline
I've shifted the Coding period to start on May 27th (with the consent of my mentor).

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

#### NumPy interactions -- July 8th to August 26th (7 weeks)
In order:
* (3 weeks)
* Mid-term evaluation, July 29th -- deliverables are:
    * bool spec implemented
    * 3 weeks of scipy interactions

#### Onward -- post August 27th
* My school begins on August 29th, so I'll cut work to around 1/3 to 1/4 of before
* Continue with features, bugs etc for the remaining weeks. slow pace.
* Final evaluation, Sept 23rd -- deliverables are:
   * bool spec implemented
   * NumPy interaction spec implemented.
* Use my now vast knowledge of Scipy to be a productive member of the community, maybe one day even receiving the honor of commit rights.

#### bonus
* Specify how to add new sparse matrix types to the existing zoo.
* axis arguments, min(), max(). Like ndarray.max() .min()?
* multidimensional array indexing 
* Represent the LU factorization obtained via SuperLU as actual sparse matrices rather than in SuperLU's internal format.
* 64 bit indices.
* performance improvements
* numpy type handling.
    * specify numpy type handling.
    * handling of sparse matrices by numpy universal functions.
>  This would involve implementation of a dispatch mechanism where
>    np.multiply knows that it shouldn't try to do things itself and get
>    it wrong, but use e.g. csc\_matrix.multiply
  

