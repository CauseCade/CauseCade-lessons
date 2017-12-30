*this lesson is under construction*

#### Converging Connection

Last lesson we saw that pass-through and diverging connections showed the same behaviour when it came to observing nodes. Is this true for any causal relations, perhaps also for Converging connections? Let's find out.

As we have a diverging connection, the simplest situation is A > B < C. This, as you will remember, corresponds
(one of the interpretations) to 2 events that can both cause a common effect. {{Let's again say we have high and low as options for each
variable (true or false would also work fine), and propose high A causes high B and high C causes high B also.}}
What can we say about B and C if we know A is high? Lets invoke our example of passing a course (from 3 lessons ago).
If you do the bonus assignment, you expect the chance of passing the course to go up.
Thus, in this context we intuitively expect B to change if A (bonus assignment) is observed to be 
true. Keep in mind we have not done the test yet, and thus do not know the ultimate outcome of the class. Would the probability of studying
hard for the test (C) change? I hope you'll agree with me in that this probability does not change. Naturally the same logic applies if we 
reason for only observing C. If we only observe B, we expect that both A and C change probability. If we pass the course, it is very likely
we have either studied hard, done the bonus assignment, or both (if we don't pass, we likely didn't do either) - so this makes sense. 


I would like to draw your attention to the fact that this is different from the Pass-Through and Divergent connections. In those cases, 
observing A (or C) only *did* change the probability of C (or A). In thoses cases, that also seemed intuitive, so what gives?
since in both cases our intuition and logic seem consistent, we can only conclude these cases must truly be different.
Let's see if this remains true when we observe node B and another node at the same time, as we did for the other connection types. 

#### Effect of other observations

We again have a diverging connection, the simplest situation is A > **B** < C. Bold face again indicates we know the state of B.
So in our example, we now know whether we passed the course (let's assume we did). Now we again observe A - what will be the case? 
Lets say we observe that we *did* in fact do the bonus assignment. Does the probability of having studied hard for the test 
remain unchanged, as in the case where we did not know B? The answer is no - in fact the probability of C decreases in this case.
This may seem strange at first. After all, how could doing a bonus assigment affect studying for a test?
(we know the events are pairwise independent - and we cannot easily see how they would (directly) affect eachother).
One way to understand this, is by realising that either event is sufficient to explain the behaviour. 
Thus if we see one of the possible causes, 'we consider' this to a sufficient explaination for the phenomenon.


Consider the following example: you own pets and keep an expensive vase in the room; you keep your pets outside the room with the vase,
but sometimes they manage to get in that room. If you one day walk into the room and find the vase broken (B)
you consider 2 possible causes: the dog broke the vase (A) or the cat did (C). Before you look around the room for your pets,
you may assign a 50% 50% change that it was the dog or the cat. If you then see the dog in the room, you probably no longer suspect it
was the cat (or at least to a much smaller degree). This has the same apparent problem: the cat does at it likes,
and does not care what the dog (or you for that matter) do. yet, observing this unrelated event (the dog in the room)
still changes its likeliness. 


This is known as **'explaining away'** in bayesian networks, as (in the example) the presence of the dog explains away why the
vase is broken (the state of B), thus changing the likeliness of the Cat having been the culprit. I think this may be the behaviour
that is toughest to accept (at first), so I recommend you give it some thought if you don't fully grasp it after the overview
in the next section.


In the next lesson we will have a brief discussion and summary of these connection types based of example 3 and discuss the implications of what we have seen.
