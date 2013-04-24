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

The project has two main parts, adding support for the bool dtype, and having better interaction with numpy. Adding bool support will start by writing a specification, implementing it along with a test suite. After this, attention will turn to Sparse Matrices interactions with other python/numpy types. The goal is functional parity with numpy's ndarrays and matrix objects.

### Timeline
* pre due date May3
* App to start time May3 to code start 
* weekly timeline 

### weekly detail 
* bool spec, spec with how other types should be handled.
* sparsetools/*.h improvement
    * bool comparisons
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
    

### Previous work with SciPy

* [Improvements to the multiply method in scipy.sparse](https://github.com/scipy/scipy/pull/516)
* [My proposed specification for boolean data type handling](https://github.com/cowlicks/scipy-sparse-boolean-spec)


### Questions
Balance between selling the project and selling my ability to complete the project.
I'm assuming a well done project proposal will imply my competence.

### Aplication tips
Links to additional information
(e.g. other projects, resources, code you've written, relevant information. You may wish to include a link to your resume here to help mentors evaluate your experience level.)
Other Schedule Information

The information requested above is generally required for us to be able to contact you and evaluate your proposal. Please feel free to add information to this template and to format it in whatever way you think will be most effective in conveying your intentions. You may wish to check with your sub-organization to see if they have any additional requirements.

We strongly recommend that you join the respective IRC channels for the sub-organizations you are applying to, and any relevant development mailing lists to the projects you are interested in working on to learn more about the community. You may wish to get your prospective mentors to read your proposals in advance so they can help you refine them.
