### Probability Lesson 2

*this lesson is under construction*

*For this lesson, I recommend viewing in: <a href="https://nemoandrea.github.io/CauseCade-lessons-deploy/" target="_blank">Separate Lesson Viewer</a>. Lessons that do not specify this should be viewed in CauseCade.*

#### Conditional Probability

*[ex.]* Let's dust off our month example again and define two events - which are sets - with one being the months of the year that have 31 days, and the other being the months of the year that have an R in the name

&Omega;={Jan,Feb,Mar,Apr,May,June,July,Aug,Sept,Oct,Nov,Dec}

L={Jan,Mar,May,Jul,Aug,Oct,Dec} 

R={Jan,Feb,Mar,Apr,Sept,Oct,Nov,Dec}

The probability of L, P(L) is 7/12, and P(R)=8/12. This should be apparent.

We determined last lesson that L&cap;R={Jan,Mar,Oct,Dec}, with probability 4/12=1/3.

Let´s now look at a case where we know something about L and wonder about the probability of R. As an example we will take that someone says that the party is in a long month. We may then be wondering what the chances are that this month contains an r. Let´s call this P(R|L).
Naturally, such an occurence should be contained in L&cap;R (we know it must be in L, and we are only looking for months with r. We could also just find the events from Omega or L and R manually).

We find that that the Probability is 4/7. Now hold on, why is it not 1/3? This is because we already know that the month is long, and are therefore looking only at 7 months. Of those 7 months, only 4 contain an R. The ones that contain and r and are long is precisely those contained in L&cap;R.
We also see that the probability of a month with r that is long is precisely the proportion that P(L&cap;R) is of (L).


Let´s look at that again.
- we found that P(L&cap;R)&ne;P(R|L) (in general)
- P(R|L) is the proportion that P(L&cap;R) is of P(L)

Below I have included a visual representation of this, which I think may clarify this point further.

*<(image)>*

This brings us to the following statement about conditional probability:


P(A|B)=P(A&cap;B)/P(B)

*notice that the bottom of the fraction contains P(B), not P(A). From the section above it should be apparent that writing P(A) there should be incorrect*

Naturally, we can rewrite this as:

P(A&cap;B)=P(A|B) * P(B)


#### Law of Total Probability

