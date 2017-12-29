*this lesson is not yet completed*

#### Basic Bayes

<(Load up example network)>

Last lesson we met our first, admittedly very boring, bayesian network. We learned how to view a few basic properties and 
how to read out what the chances are of each state for each node (random variable). One thing that was missing, as you may have 
have noted, was any application of Bayes' rule! Don't worry, we will get to that right away. First, make sure the example 
network for lesson 1&2 is loaded. 

As A and B are not independent, the probability of B given a certain state of A (which we will call P(B|A) - 'probability of B 
given A') is different from B without any knowledge of A. This is what we derived in the previous course. In this case we will 
start by looking at P(B|A), we will visit P(A|B) later on. These probabilities are known as the *conditional probabilities*, as we asses the probability of (say) B under the *condition* that A is in a certain state. Lets start by looking at the possible configurations.

We have: P(B=0|A0),P(B=0|A1),P(B=1|A0),P(B=1|A1), with A0,A1 referring to a particular *observed state* of A. P(B=a)
refers to the probability of B being in state a. 
In statistics, all the values P(B|A) (which refers to all the conditional probabilities, and will 'contain' 4 entries in the above 
case).  To display P(A|B) in a convenient fashion we will display it in a table form. This table we will call the Conditional
Probability Table, or CPT for short. Note that this table format of the CPT is just to facilitate human interpretation, and the matrix appearance is therefore not fundamental. Why don't you try viewing this? To find it, select node B and then go to
the edit menu (top left), and select *view/edit CPT*. If you have selected B, you should see the matrix P(B|A) appear. As
you can see the various values of A appear in the horizontal dimension of the matrix and the values for B in the vertical 
dimension. One logical property of this matrix is that the columns should sum to one.

*Lets say we know A is in state A0, then we wish to know the probability of each **state** of B. In other words we simply wish 
to know P(B0|A0) and P(B1|A0). These are naturally the values of the (in this case) first colum of our CPT. This 
is a consequence of how we defined our CPT. The values P(B0|A0) and P(B1|A0) should sum to one for obvious reasons (B 
must be in either state 0 or 1). This is analogous for any colum of a CPT.*

For each connection between nodes (random variables) we have such a CPT. You may wonder why we dont specify two CPTs, as we may not only want P(A|B) but also P(B|A). Here is where the power of bayes rule comes in. If we known P(A|B) and P(A) and P(B), we can just compute P(B|A)! Thus, we don't need to explicity define P(B|A). You may then wonder which one we specify, if either one will do? In our network we always choose the CPT that is consistent with the *directionality* of our network. That is, if you see an arrow pointing from A to B, then we have P(B|A) specified. Keep in mind this is just so that we have some consistency in our approach (which simplifies computation), but we may just as well specify P(A|B). 

Okay, that's great and all, but what about that P(B) and P(A)? If we only specified P(B|A) in our example network, then that doesn't help us find P(A) or P(B) if we don't know either. Let's tend to this problem later and pretend we know P(A). How would we then compute P(B)? Luckily this is fairly straightforward as we already know P(B|A) (this one is directly specified in the network!). We can then use the Law of Total Probability to compute P(B). 


*[Ex.] P(B)=P(B|A0) * P(A0) + P(B|A1) * P(A2) is what we would use. Try computing the Values for P(B=1) and P(B=0) by hand yourself, using that P(A=0)=0.8 and P(A=1)=0.2. (Remember that you can find the CPT by selecting node B and going to 'edit linkmaxtrix'.) This is also what the network has currently loaded, so you can check your answer by clicking on node B and seeing if the probabilities match.*

If everything has gone well, your answer should match that of the network. Let's now have a look at how we would get to that P(A) that was just given in the previous exercise. As you can see, node A has no arrows pointing towards it (i.e. it is a *root node*). For such  a node we have a so-called **prior probability** or prior for short. One definition of this is as follows: "a probability as assessed **before making reference to certain relevant observations**, especially subjectively or on the assumption that all possible outcomes be given the same probability." I have highlighted the key part for you. 
For a root node, we specify this prior probability. It can be viewed as a guess of what the probabilities are. In the case of the weather it may for example reflect the observed frequency of rain in a given time period. Maybe we know that in february, the chance of rain on any day is 23%. We could then set this as a prior probability. 
<(I like to see this prior probability as a consequence of a pseudo-node that is above each root node that reflects the universe. So you would have [Universe->]Rain->Garden is wet. I wouldnt think too much of this, but for me it can be helpful to visualise it as such.)>
For consistency's sake, we do still specify a CPT for a root node <(Why don't you check it our for node A?)>. Looking at this CPT, you should see it is the identity matrix (1's on the diagonal, 0 elsewhere). This does not reflect anything fundamental, it is just so that we can efficiently set P(B) by multiplying our prior probability with said CPT. This is particular to this implementation, and we may just as well specify our prior directly.

*[Ex.] Let's try changing the prior probability for A and see how B changes; try computing this by hand first and see if you answer matches what the network devices. Tip: it should be very similar to the previous exercise*

Alright, so let's recap what we have done here. We met the CPT, which is simply the conditional probabilities of nodes, and we met the prior probability and saw how probabilities change. 

In this lesson, we only looked at how probabilties change going in the direction of the network (i.e. in the direction of the arrows). In the next lesson, we will look at going the oppposite direction. This is where we will invoke Bayes' rule.
