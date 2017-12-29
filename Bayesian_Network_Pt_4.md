*this lesson is under construction*

#### More nodes & Independence

Last few lessons we have focussed on cases where we only had 2 nodes. In such a case the relationship between nodes is simple:
either the nodes are independent (knowing the state of one does not influence the probability of the other) or not.
If they are not independent, this may be due to a causal relationship (e.g. rain causes the grass to be wet),
or due to a deterministic relationship (e.g. if the species random variable is of type feline,
it follows that it is also of class: mammal - though one would be hard pressed to find anyone saying either of these causes the other). Things become a little more complex once we introduce more random variables (i.e. nodes).


Before we do that, let's look at independence in our trusty old two node system. As we briefly mentioned in the earlier sections, two nodes are independent if knowing the state of one does not change the probabilities of the other random variable. Putting that into a more formal statement, we find that the following (for 2 random variables) must be true:

P(B|A)=P(B)

or, equivalently 

P(B&cap;A)=P(B) * P(A)

*revisit the probability course if you dont see why this is true*

