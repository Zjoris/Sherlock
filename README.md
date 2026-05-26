# Sherlock

Teaching a model to ask meaningful questions. (Inspired by black stories game).

* Given front card (vague description) generate several ``full stories" (sample of set of all possible worlds)

* given several ``full stories", generate a polar question

* With answer eliminate non-agreeing stories (possible worlds), possibly generate new stories that are different but agree with context.
  * Or use answers as topological notion of evidence. In theory this should result in Topology with FIP so we should be able to eliminate worlds without issue. Unless we want to model a 'lying' environment as well, in which case the resulting topology that need not have FIP.

* Do this until you have a story that falls in the same ``similarity class" as target story.
* Use number of questions asked as performance metric? Or perhaps any time you get confirming answer to polar question?
* Repeated interaction between model and environment (asking polar questions and getting yes/no): RL.


## RL for questions (abstract/logical)

There is some infinite set of worlds $S$ (each world represents a possible story (which could be charachterized by Prop logic?)), with $S^*\subset S$ as the similarity class of target stories. We sample a finite set from $S$, call it $\^{S}_0$, which is our initial thoughts of what the story could be. ($\^S_0$ can be seen as a similarity class as well). We give a partition of $\^S_0$ which corresponds to a polar questions. Based on yes/no answer we eliminate worlds from $\^S_0$ and may sample new ones from $S$ resulting in $\^S_1$. We keep going until $\^S_n = S^*$. Or something along the lines.

### Performance measures

* Less questions is good? Faster the better?
* The more specific the better?
* The more "yes" answers the better?
* The less worlds that need to be generated/sampled the better?
