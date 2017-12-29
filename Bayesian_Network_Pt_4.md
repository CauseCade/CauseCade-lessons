*this lesson is under construction*

#### More nodes & Independence

Last few lessons we have focussed on cases where we only had 2 nodes. In such a case the relationship between nodes is simple:
either the nodes are independent (knowing the state of one does not influence the probability of the other) or not.
If they are not independent, this may be due to a causal relationship (e.g. rain causes the grass to be wet),
or due to a deterministic relationship (e.g. if the species random variable is of type feline,
it follows that it is also of class: mammal - though one would be hard pressed to find anyone saying either of these causes the other).
Things become a little more complex once we introduce more random variables (i.e. nodes).


Before we do that, let's look at independence in our trusty old two node system. As we briefly mentioned in the earlier sections,
two nodes are independent if knowing the state of one does not change the probabilities of the other random variable. 
Putting that into a more formal statement, we find that the following (for 2 random variables) must be true:

P(B|A)=P(B)

or, equivalently 

P(B&cap;A)=P(B) * P(A)

*revisit the probability course if you don't see why this is true*

#### Relationships between multiple nodes

The relationship between nodes when we have more than 2 random variables may not be so simple. Below I have listed some examples
that demonstrate some of the phenomena we will discuss in the next sections. Further clarifications will follow in the next lessons.
[ex1] Let's take as an example the following three random variables:

1. you completed a bonus assignment
2. you studied hard for the test
3. you passed the course

Here, we can see that, intuitively, both 1 and 2 can 'cause' 3 to be true (if you complete the bonus assigment or study
hard you will get a higher grade and thus pass the course). So, let's say we completed the bonus assignment,
we know we are more likely to pass the test. In other words, node 1 and 3 are not independent. 
Naturally node 2 and 3 are likewise not independent. Node 1 and 2, however, are independent if you have not done the test yet
(i.e. you dont know your grade yet) (one could argue you have finite time to spend on class, and thus they are not independent - but
let's keep it simple). This seems to be consistent with your intuition, as there is no (apparent) causal (or deterministic)
relationship between doing the bonus assignment and studying hard for the test.


Note that here that the 3 random variables are not all independent (i.e. P({1}) * P({2}) * P({3}) =/= P({1}&cap;{2}&cap;{3}).
So, while 1 and 2 may be independent, the whole network is not.

[ex2] Let's look at another example. We have the following three random variables:

1. It is snowing.
2. You are cold.
3. You arrive late.

If we again use our intuition we see that this case is similar to the above but different in a critical way. In this case,
1 causes both 2 and 3. So rather than 2 'causes' for one random variable, we have 1 'cause' for two random variables.
(or 1 cause and 2 effects if you will - though I will stress that one must be careful with interpreting causal relations,
we will revisit this later). Intuitively, if it is snowing we expect the chances of being cold and being late to go up.
This is similar to the previous examples in that by studying hard we could increase the chance of passing. In this case, if we do not
know whether it is snowing, we may intuitively be able to infer that if we are late, it is also more likely that we are cold.
Notice how the opposite was true in the previous example. If this seems a little strange right now, do not worry,
we will spend the next section discussing this in detail.

[ex3] Let's do one final example. We have the following three random variables. We toss two coins, our random variables are:

1. Coin 1 is heads.
2. Coin 2 is heads.
3. Both coins have the same face up.

After some thinking you should see this is similar to example 1, as both coins 1 and 2 can be interpreted as 'causing' the state of 3.
Note in this case it is a deterministic relationship, rather than a traditional (event 1 results in event 2 after a time) causal
relationship (as in ex1). Again, we see that 1 and 2 are independent events (this time there is no doubt about it). However,
this time also 1 and 3 (and 2 and 3) are independent. So in this case, all nodes are pairwise (per 2) independent,
but not mutually independent (independent as a whole). So again, P({1}) * P({2}) * P({3}) =/= P({1}&cap;{2}&cap;{3}).


Note that this makes sense, as 3 follows deterministically from 1 and 2, thus P({3}) follows deterministically from {1}&cap;{2}
(the combination of 1 and 2). Therefore the whole network cannot be independent. 


In this section we have seen that independence relationships are not so simple when we have more than 2 random variables.
We have seen that there is a difference in idependence with different causal relationships.
In the next sections we will explore this in more detail with probabilistic formalism. 
