*this lesson is under construction*

#### Overview

So last lessons we saw the behaviour of the three causal relationships between events that we could come up with. 
We also noticed any causal relationship could be constructed from these 3 basic types. We also noted that The divergent and pass-through
behaved in similar manners when it came to 'blocking' paths (through which 'information flows'), while convergent connections behaved
differently. We also noticed that whether a path is 'blocked' dependent on whether a certain node is observed.

*For a three node system of type A-B-C:*

we noticed that for divergent and pass-through connections evidence:
- can pass from A to C, if B is not observed
- cannot pass from A to C, if B is observed
 
we noticed that for convergent connections evidence:
- cannot pass from A to C, if B is not observed
- can pass from A to C, if B is observed
 
As you can see, the convergent connection behaves opposite to that of the divergent and pass-through connection.
Remember that this is because of the fundamental difference in these types of causal relationships,
and that this behaviour is logical from an intuitive point of view. 
 
#### conditional independence
 
As mentioned in lesson 4, we would discuss the concept of conditional independence in more detail. The fact that random 
variables are independent depending on whether a third random variable is observed or not is a case of conditional independence.
It may seem strange that two random variables which are independent if you do not observe any other random variable,
but are not longer independent when you observe a (specific) third random variable. Let's first get some things out of the way:


Conditional Independence (A and B are conditionally independent if):

[1] P(A&cap;B|Y)=P(A|Y) * P (B|Y) 

or, equivalently

[2] P(A|B&cap;Y)=P(A|Y)


Let's have a look at these two (equivalent) conditions for conditional independence.

One way to interpret the first one would be to view this as saying that the probability of A and B can solely be explained/determined
by the state of Y, and that their joint probability is simply their individual probabilities under Y. Analogous to simple mutual
independence in the probability course, A and B are independent, *but now given the state of Y*. 


One way to interpret the first condition, is that the probability of A, given both B and Y is simply the probability of Y, or in other
words: the state of B does not affect the probability of A. That is A and B are conditionally independent.
(B does not affect A under the condition we know Y)


It also follows from the definition that two events may be conditionally independent, but not necessarily independent. 
In fact, a diverging or pass-through connection is a situation where two events are conditionally independent
(think about what we learned about these connections and how they satisfy the conditions for conditional independence),
but not independent. An example of two events that are conditionally independent and also independent is: The day of the month is odd,
a coin toss is odd, you are seated facing north. 

#### Conditional Dependence

Conditional dependence can be interpreted as the opposite of conditional independence (from a point of view). Rather than two variables
being independent if we know the state of a third variable is observed, the two variables are independent as long as we do not know
anything about this third random variable. If we do observe the state (or obtain knowledge about the state of this random variable)
then the two random variables are dependent.

No formal definition is available, but in the case that we have two event A,B that each increase the probability of C, the following
must be true if A and B are conditionally dependent:

P(A&cap;B)=P(A) * P(B) (true for any conditionally independent pair)

and

P(A|B&cap;C)<P(A|C) (true for specific case)


This is explaining away. In bayesian networks, conditional independence of two random variables is represented visually by a converging 
connection. As we looked at in the lesson on converging connections, if we interpret the random variables as causally related events,
this property of explaining away is intuitive. 

#### Summary and outlook

Thus, random variables may be:
1. conditionally independent & independent (completely unrelated events) [...]
2. conditionally independent & dependent (diverging & pass-through connection)
3. conditionnally dependent & independent (converging connection)


In the next section, we will have a look at how this conditional independence functions in larger networks.
There we will also see how the directed network form of bayesian networks allows us to easily interpret dependencies. 


