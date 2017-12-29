*this lesson is not complete yet*

#### From humble beginnings

To start our journey, we will lay out the simplest network we can imagine: the two random variable network (save for the 1 
random variable case - but it should be obvious we cannot use Bayes' rule in this case!).
Firstly, load up the example network for this lesson. As you can see, the network is a simple as it gets; just 2 nodes and a
single link connecting them. For now, I have called them node A and node B, to avoid any semantic or intuitive problems. The
abstract nature of the names will hopefully help you focus on the concept behind it. A little side note: in probabilistic
terms: a node in the network represents a random variable, and a link means these random variables are not independent. 

Let's tackle a question that may have arisen by now: in our derivation of Bayes' rule, we did not specify a 'directionality' of 
random variables, yet here we observe an arrow pointing from A to B. We will come back to this point in a later lesson, so 
rest assured this point will become clear later on. Similarly, any confusion on independence will also be cleared up in a later
lesson.

With that out of the way, let's have a look around this network. If you click on node A (clicking twice will unselect it, so 
keep that in mind), you will see the overview window appear in the left hand of the screen. The first thing I would like to
draw you attention to is the bar chart with the probabilities. Each state of this node (random variable) has a probability
between 0 and 1(1), and summing over all states will yield 1 (2). This is naturally nothing more than the 
simple consequence of each node being a traditional variable. While it may be in a 'network´ structure and many nodes 
are connected, each node is ultimately a random variable and, as such, adheres to all the concepts we set in the previous chapter.

*To illustrate this point with an example, lets take node A to be whether it rains or not. A0 and A1 would then for example be 
true or false (or rain & no rain if you prefer). The chance for A0 (rain) can naturally not exceed 1. (intuitively explaining 
(1)) and the chance of A0 and A1 should sum to 1, as it **must** rain or not, there is no third option. (explaining (2))*

Below the probability of the node, we see the node status. The first property of a node is whether this node is a *root node*. 
One intuitive way of interpreting this property is viewing it as the node having parents (i.e. a node with a direction pointing
towards it) or not. <expand>
  
The second property we see here is whether the node has evidence. When I say evidence, I mean that an observation has been made 
about the state of this node. In the rain example, it would be (for example) observing that, unfortunately, 
it is raining outside. Such an observation can be made about *any* node in the network (as each are random variables). 
In practice, it is often that the random variable of interest cannot directly be observed, or is yet to (maybe) occur. 
It should be noted that while my example used a ´hard´ observation (i.e. P(rain)=1,P(no rain)=0), it is possible to make 
an observation that does not have one state at P=1 and all the others at P=0. <We will view this in a later lesson>. You
may wonder how an observation may affect a more complex network, but rest assured, we will cover this in our lesson on 
independence.
  
Even further down below in the overview menu, we see a section named 'parent nodes' and 'daughter nodes'. This serves as a 
quick way to navigate the network, and contains no properties of the node. Clicking a parent node here will set the current
node selection to that node, which means the overview component will then display info about that node. This is completely
equivalent to clicking that node in the network itself.

With the very Basics out of the way, let's take our steps into conditional probabilities.
