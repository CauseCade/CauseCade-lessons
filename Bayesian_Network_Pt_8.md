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
 
The fact that random variables are independent depending on whether a third random variable is observed or not is a {...}
 
#### D separation
 
As mentioned above, we can construct **any** network from these three basic causal relationship types. This means that we can easily
determine whether two random variables are independent, given the set of observations, provided we have the network structure. (keep in
mind the network structure is just a *representation* of the underlying dependence relationship of the random variables).
We simply have to analyse the possible paths from our starting node (let's call it X) to our other node (let's call it Y) and see if,
using our rules above, we can have 'evidence' pass from X to Y. In the simplest bayesian networks that can be computed exactly,
only one path is possible(depending on the state of the random variables), as the *directed* and *acyclic* nature of such network 
requires. <{examnple}> 
 
 
So, what do we have to look out for when checking this? We have to first find the path from X to Y.
This should be fairly straightforward. (in the case of multiple paths, all *possible* paths should be considered).
Having done this we must first check if we have any observed nodes. That is, any nodes whose exact state has been observed.
In that case, we know that a connection of type Pass-Through or Diverging, will not allow 'evidence' to pass through. In other words,
if we have X > U > Y or X < U > Y, with U observed, any observations about X will not affect (the probability/state of) Y
(i.e. no evidence can pass from X to Y). Likewise, we have to consider the case for converging connections, as they may also
'block' the passing of evidence. If we have X > U < Y, with U *not* observed we know X cannot affect the state of Y. Naturally,
any other nodes may be in between X and Y besides U. We simply check for each random variable on our path whether evidence
can pass through. 
 
 
As an example, lets take X < V < **U** > Y, with U observed.  Can any observation of X affect Y? The answer would be no,
because while V allows evidence to pass through (unobserved pass through), U does not (observed diverging),
thus allowing no evidence to pass through. If any point along the path is blocked, the path as a whole is blocked.
Let's look at another simple example. We have: X < V < U > **O** < Y. Can any observation of X affect Y? The answer would be yes,
as V and U will allow evidence to pass through, and while O is observed (which caused problems in the previous example),
in the path we are analysing O is a converging connection. Therefore O allows evidence to pass through. 
 
 
So, let's introduce some of the terminology for this. The set of observed nodes is traditionally referred to as Z.
If you have a converging connection, where no evidence of the common effect is present (i.e. the common effect has not been observed, 
or an effect of this effect has been observed), this is known as a collider, as it does not allow evidence to pass through (see above).
Connections that do not have this property (which are naturally the diverging and pass-through type) are called non-colliders.
With that out of the way, the formal definition of D-separation is as follows:
 
 
*"If G is a directed graph in which X, Y and Z are disjoint sets of vertices, then X and Y are d-connected by Z in G if and only 
if there exists an undirected path U between some vertex in X and some vertex in Y such that for every collider C on U, either C
or a descendent of C is in Z, and no non-collider on U is in Z."* 
 
 
Don't panic, this says the same thing as what we worked out in the paragraphs before it. **Two nodes would be D-separated if
the above is not true.** For completeness, we will see how this formal definition matches our own. We have X and Y as before and now
Z is the set of observed vertices (i.e. random variables / nodes). (in our previous examples this would have been U, and O).
they are D-connected only if a undirected path (naturally the graph *itself* is directed, but our path may go against and
with the direction of the graph, thus we seek any path - not a directed path, which would imply only going with the direction
of the network) exists with certain conditions. So far this seems consistent with what we had before.
We then have to conditions: 1) for every collider on this path (i.e. converging connection) either this collider itself
(the common effect) or a descendant (an effect of this node) is in Z (i.e. has been observed). If you find this strange,
re-read the section on converging connections. 2) none of the non-colliders (i.e. diverging and pass-through) is in Z 
(i.e. is observed). I hope you see this is identical to what we determined above.

 
For this lesson I have created a larger network (click the load network for this lesson button), and I encourage you to try to see if you can determine which nodes are D-separated and which (pairs of) nodes are D-connected. Also consider what would happen if you measure/observe some of the nodes in the network - which D-separated pairs of node will now become D-connected, or vice versa?
 
 
What I'd like you to take away from this is that when two nodes/random variables are D-connected, observing one of the two will affect
the probability distribution (i.e. the probabilities of each state) of the other. If they are D-separated, 
the two nodes are independent. Next lesson, we will get back to our probability formalism and actually put the qualitative
arguements made here into numbers. Doing so will enable us to describe the concepts mentioned here in a quantitative manner,
and if you understood everything up to now, putting in the numbers should be a breeze.
