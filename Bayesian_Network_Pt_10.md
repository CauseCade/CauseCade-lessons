So far we have looked at the independence relationship quantitatively, but let us now return to probability.
Load the demo network for this lesson above. We can see the network consists of 5 variables. Additionally, we can see
from the direction of the edges that we have two variables which are conditionally independent given
*mesenchymal migration* (the 'effects') and two variables that are conditionally dependent given said variable 
(the ´causes´).

What we wish to represent is the JPD. This JPD would contain all the information about the relationships between the
variables. We will denote each variable with the first letter leading to the following sought JPD: P(I & M & E & S & C).
Note that this is of course not one value but a distribution. We will rewrite this as a CPD (which is equivalent to
the JPD). The CPD, in full, is: P(I|M & S & C & E)P(C| M & S & E)P(M|S & E)P(S|E)P(E). Note that this CPD is not unique.
I have chosen for this form going from the bottom of the graph to the top. This CPD is not all that much simpler
than the JPD, in fact it looks more complicated. 

We can, however, use conditional independencies to simplify this CPD into a more compact expression with fewer parameters.
We just have to know said independencies. Luckily, we know how to read those from the bayesian network! Let's go over
the CPD terms to view what they reduce to.

P(I|M & S & C & E) becomes p(I|M&C) as the terms S and E are conditionally independent from I given M 
(pass-through connection). This further reduces to P(I|M&C)=P(I|M) as C is conditionally independent from I given
M (diverging connection)

P(C|M&S&E) reduces to P(C|M) as the terms S and E are conditionally independent from C given M 
(pass-through connection).

P(M|S&E) remains unchanged as there is no conditional independence statement here (converging connection).

P(S|E) reduces to P(S) as E is conditionally independent if we do **not** know M (i.e. not given M)
(converging connection).

P(E) remains unchanged. (as it is not a conditional probability.

So let's have a look at what remains of our CPD expression: P(I & M & E & S & C)=P(I|M)P(C|M)P(M|S & E)P(S)P(E). This is
a lot less scary than the more general expression above. Note that we were able to quickly read the conditional
independence conditions from looking at the bayesian network structure. Below we will do some calculations with this.

#### Inference

