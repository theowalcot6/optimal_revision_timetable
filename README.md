# optimal_revision_timetable
Can we use simulated annealing, an advanced optimization technique, to build an optimal revision timetable?

We are looking at the problem of creating an optimal revision schedule for students studying for their exams (A-Levels, AS, GCSEs, etc.)

**Schedule Space:** The phrase we will use to describe the availability of time between now and the final exam date, the different subjects that can be studied in that time, and the different activities that can be completed. We can accurately determine how much effort is needed for a student to raise their score from their current score to their target score. All we need is their learning speed which is largely a statistical approximation problem.

**Permissible Effort Units:** A measurement used to describe the amount of effort a student requires for each exam to reach their target grade. We want to achieve the permissible effort units required in a minimal amount of time. If this allows us padded time, then we can do additional studying to maximize our confidence in subjects, using a mathematical approximation on priorities. However, optimizing the schedule space (when to do that effort and on what) is by no means a linear operation. When completing an action, achieved permissible effort units might change depending on time to the exam, loss of learning curve (how does the retention of the subject fall after it's learned and how in each subsequent learning), number of hours spent revising already that day. In other words, actions aren't homogenous, and we can't apply linear optimization techniques to work out the optimal revision schedule.

If you think about the problem, an exhaustive search would be computationally infeasible
Example: If you have 400 hours (200 study segments) for Maths and 200 hours (100 study segments) for English. The revision schedule consists of 60 possible days each with 6 segments = 360 study segments. This is an extremely large problem to solve in relation to pure permutations. Therefore, we will look at a stochastical optimization approximation technique.
