*this lesson is under construction*
*notes: expand on acyclic*

#### Types of relationships between nodes

Let us briefly explore what kind of relationships we can have between nodes. For this we will use a network representation of the nodes,
with the directions of the arrows indicating a causal relationship (in the direction of the arrow). We recognise 3 different cases. 
Note that we implicitly do not allow cyclical connections. (this will be important later)

#### Converging Connection

A > B < C

This is the type of connection that we have seen in example 1 and 3. We have two events (A and C) that both cause B.
I hope it is obvious that such a causal relationship is a common occurence in the world. Note that we are not restricted to 2 causes,
we can easily have many causes having one combined effect. *The central concept is that multiple causes have one common effect.*
This means that if we observe the effect, we cannot attribute it to a single cause. More on this in a future lesson.

<(image)>

#### Diverging Connection

This is the type of connection that we have seen in example 2. We have one event (B) that causes both A and C. In other words,
the cause B has two effects. Again, this is nothing outworldish and as example 2 demonstrates, a thing often observed in life.
As in the diverging connection, we are not restricted to 2 consequences. We can easily have 1 cause that has 50 effects.
*The central concept is that one cause has multiple effects.*

A < B > C

<(image)>

#### Pass-Through Connection

This type of connection we have not featured in an example. In this case we have an event A that then affects B which then causes C.
You can also see this as A causing C, through the mediator B. An example would be A:eating spoilt food, B:some biological process,
C:feeling ill. We could reverse the order of the causal relationships (to complete the 4 different possible arrangement
of the causal relationships) but we see it simply the same **type** of connection (pass-through).

A > B > C or A < B < C

<(image)>

*naturally we can also rearrange the order of the nodes, but the point of this is to show which **types** of connections can exist.*

#### Combining this in a network

With these three types of connection, we can make any network structure. I have shown an example below, with the different types of 
connections indicated in the image. Note that because we only have three types of causal relationships, we only need to know what each  
connection means for independence to determine the indepence of any two pairs of node in the network.

<(image)>

So we have seen that there are only 3 types of connections we can make in a causal network of this type, and with this we can
represent anyacyclic causal relationship of as many random variables/events that we like. In the next lesson we will look at
the Diverging and Pass-Through connection in greater detail.
