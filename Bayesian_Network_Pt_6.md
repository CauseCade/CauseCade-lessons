*this lesson is under construction*

#### Diverging & Pass-Through Connection

We will now have a closer look at 2 of the 3 types of connections we have seen last lesson. The reason why I grouped these
connection types will become apparent below. Remember that these connections represent the way events/random variables can be related.


At first sight a diverging and pass through connection may seem no more related than the converging and pass through connection - 
after all they both share one 'causal arrow'. Trying to reason using our intuition also does not help too much. If we look at the 
behaviour of each variable when making observations, we may be able to figure things out. 


Let's think about the diverging case first. Let's for convenience assume we have A < B > C as a relationship. Lets also say we have high 
and low as options for each variable (true or false would also work fine), and [1] propose high B causes high C and A. What would you 
expect C to be in if you only know that A is high? Naturally, you would reason that C is also high. This is because with A high,
we reason this must mean the cause (B) must also be high, and if B is high, then C (which is an effect of B) must also be high.
So as it were, we first reasoned what the starting event (in the case of causality, where the cause precedes the effect - not true for
deterministic events) was, and then figured C from there (using [1]). Similar reasoning applies for knowing C. 


Now, let us look at the pass-through case, and see if this is any different. We have A > B > C as a relationship.
We propose [2] that High A causes high B, high B causes high C. So, if we have high A, we have high B and consequentiall high C. What if 
we only know B is high (nothing known about A,C)? Well, it should apparent C is high. We can also reason that if B is high, this must be 
because the cause (A) is also high. Thus, A must also be High. If we only know C is high, then we reason twice about the cause and find 
that A and B must both be high also. 


So, let's look at what we saw. For both diverging and pass-through connections, if we observe *only* one of the variables,
the other ones become more likely to be high as well (under the specified relation). In both cases this was because we
could reason that either the other node is an effect of the node we know the state of (and if we know the cause we must know the effect,
right?) or the other node is a cause of the node that we know the state of (in which case we can deduce the state the cause must
have been in *in order for us to see this effect*). Looking at it that way, this seems fairly intuitive,
is it perhaps always true for any causal relation? No - we will see next lesson that this does not hold for converging connections,
but for now let's leave that for later.

#### Effect of other observations

We have also seen that both diverging and pass-through connections behaved in the same way, even though the underlying causal relation 
may *appear* different at first sight. We looked at a case where we only knew/observed one of the nodes/random variables and had to 
infer the state of the others. Let's have a look at the case where the centre node (or any for that matter,
but the middle will produce interesting results - for reasons that will become apparent).

[1] Looking at the diverging case, we now observe the state of node B (let's say High) leaving us with: A < **B** > C
(Bold indicating that we know the state of B). Does observing the state of A now help us infer the state of C? B is naturally not
affected by any observation of A.The correct answer would be: no. To think of why, you should go back to the case where it did.
Above, we could infer the state of C because through our observation of A, we could predict the state of the 'cause' (B)
and subsequently reason about the effect on C. Here,
this does not work, as the state of B is already fixed, thus observing A does not change anything about the cause and
therefore does not affect C (it's effect). I hope this makes sense intuitively. If not, try to think of the snow example.


If we know it is snowing, observing that it is cold will not make it any more likely that you will be late. (if we did **not**
know it was snowing this observation would make it more likely that you will be late). Note that while observing that you are cold
will not make it *more likely* that you will be late if you know it is snowing (B is known), this **does not mean the probability
of being late is higher in the case where we do not know it is snowing**. The reason, as mentioned above, is because this observation 
does not affect the common cause of these observations (A,C) - as it is already 'fixed' (observed). Thus, the 'path' of evidence
(observing A: you are cold) going to C is 'blocked' by the observation of B, the common cause. 

[2] looking at the pass through case, we now observe the state of node B (let's say High) leaving us with: A > **B** > C. Again,
does observing the state of A now help us infer the state of C? The correct answer would be: no. To think of why,
you should go back to the case where it did. When we observed A, we could reason that B would be high (caused by A),
and C would be high (caused by B). In this case, however, observing A does not change the state of B (it has been observed)
thus any changes to A do not affect C. (as A cannot affect the cause of C). The same holds if we observe C.
Any observations of C before allowed us to reason about the (probable) state of the cause and subsequently about its cause (A).
In this case, any observation of C does not change the probable state of B (as it is already observed),
and can consequentially not affect the state of A. Here too, we see that the 'path' of evidence (observation of either A or C)
is blocked by the observation of B, the causal mediator (or central link in this causal chain - view it as you wish).

#### Things to take away

So let's think about this. When we only made one observation, both the pass through and the diverging connections showed the same
behaviour. When the 'central' node/random variable (common cause, central link) was observed,
in both cases the nodes that before *could* affect the state of the other nodes in the network, can now no longer. In both cases, this matched with our intuitive concepts of how causality works. Note that this is true for any causal relation of this type, not just the specific examples. Note also that this will work for any kind of causal relations, not just strict boolean ones (e.g. if it snows it may be the case that the chance that you are late is 70%, whereas if it doesnt snow it is only 15%) - we will look at numerical examples later on.

So we have seen, from a certain perspective, these two types of connections are identical. I hope it now apparent why I grouped them in this lesson. In the next lesson we will look at the converging connection type, followed by a discussion.
