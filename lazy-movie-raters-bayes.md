Lazy Movie Raters
Netflix Probability Interview Case (Bayes’ Theorem)

                                     Business Context

User ratings strongly influence recommendation systems on streaming platforms like Netflix. However, not all user feedback is equally reliable.Some users consistently provide
positive ratings regardless of content quality,introducing bias into predictive models.This case demonstrates how Bayesian probability can be used to infer hidden user behavior
from observed rating patterns.

Problem Statement

80% of Netflix users are normal raters
Probability of thumbs up = 60%
Probability of thumbs down = 40%
20% of Netflix users are lazy raters
They rate 100% of movies as thumbs up
Question:
If a user gives 3 consecutive thumbs up, what is the probability that the user is a lazy rater?

Let:
- **L** = user is a lazy rater  
- **N** = user is a normal rater  
- **T** = three thumbs up in a row  

\[
P(L) = 0.20,\quad P(N) = 0.80
\]
\[
P(T \mid L) = 1
\]
\[
P(T \mid N) = 0.6^3 = 0.216
\]

Using Bayes’ Theorem:

\[
P(L \mid T) =
\frac{P(T \mid L)\,P(L)}
{P(T \mid L)\,P(L) + P(T \mid N)\,P(N)}
\]
Calculation
\[
P(L \mid T) =
\frac{1 \times 0.20}
{(1 \times 0.20) + (0.216 \times 0.80)}
=
\frac{0.20}{0.3728}
\approx 0.536
\]

Final Result
> **Probability the user is lazy given three thumbs up:**  
> \[
> \boxed{53.6\%}
> \]
