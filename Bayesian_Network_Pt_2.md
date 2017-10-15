*this lesson is not yet completed*

#### Basic Bayes

Last lesson we met our first, admittedly very boring, bayesian network. We learned how to view a few basic properties and 
how to read out what the chances are of each state for each node (random variable). One thing that was missing, as you may have 
have noted, was any application of Bayes' rule! Don't worry, we will get to that right away. First, make sure the example 
network for lesson 1&2 is loaded. 

As A and B are not independent, the probability of B given a certain state of A (which we will call P(B|A) - 'probability of B 
given A') is different from B without any knowledge of A. This is what we derived in the previous course. In this case we will 
start by looking at P(B|A), we will visit P(A|B) later on. Lets start by looking at the possible configurations.

We have: P(B0|A0),P(B0|A1),P(B1|A0),P(B1|A1), with A0,A1,B0,B1 referring to a particular *state* of A and B respectively. 
To display this in a convenient fashion we will put this in a matrix form <(which we will call P(B|A))>. The values for this
matrix can be found in what <(I call the linkmatrix)>. Why don't you try viewing this? To find it, select node B and then go to
the edit menu (top left), and select *view/edit linkmatrix*. If you have selected B, you should see the matrix B|A appear. As
you can see the various values of A appear in the horizontal dimension of the matrix and the values for B in the vertical 
dimension. One logical property of this matrix is that the columns should sum to one.

*Lets say we know A is in state A0, then we wish to know the probability of each **state** of B. In other words we simply wish 
to know P(B0|A0) and P(B1|A0). These are naturally the values of the (in this case) first colum of our linkmatrix. This 
is a consequence of how we defined our linkmatrix. The values P(B0|A0) and P(B1|A0) should sum to one for obvious reasons (B 
must be in either state 0 or 1). This is analogous for any colum of a linkmatrix.*
