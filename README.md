# Sherlock

Teaching a model to ask meaningful questions. (Inspired by black stories game).

* Given front card (vague description) generate several ``full stories" (sample of set of all possible worlds)

* given several ``full stories", generate a polar question

* With answer eliminate non-agreeing stories (possible worlds), possibly generate new stories that are different but agree with context.
  * Or use answers as topological notion of evidence. In theory this should result in Topology with FIP so we should be able to eliminate worlds without issue. Unless we want to model a 'lying' environment as well, in which case the resulting topology that need not have FIP.

* Do this until you have a story that falls in the same ``similarity class" as target story.
* Use number of questions asked as performance metric? Or perhaps any time you get confirming answer to polar question?
* Repeated interaction between model and environment (asking polar questions and getting yes/no): RL.
