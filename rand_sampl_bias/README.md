# Randomness, sampling, and selection bias
The concept of probability is fundamental and the ability to quantify uncertainty—to go from a vague  "maybe" to a clear and precise "65% chance of____ with a margin of error of 3%." Quantified uncertainty not only defines what is known; it also specifies how confident you can be about that knowledge.

## Randomness
Randomness can be defined as the apparent lack of pattern or predictability in events. A random sequence of events, symbols, or steps often has no order and does not follow an intelligible pattern or combination. Individual random events are, by definition, unpredictable. But because they often follow a probability distribution, the frequency of different outcomes over numerous events (or trials) is predictable.
it is important to leverage the concept of randomness to gather a representative sample from the population. Using randomness, each element of a population has an equal chance of being chosen for the sample.

## Selection bias
Differences between the sample and the population are known as selection bias. If the sampled individuals differ from the others in important ways, such as spending rates or purchasing behavior, the knowledge gained from their data might not apply to all customers.

## Dependent versus independent events
When talking about probabilities of events, whether Bayesian or frequentist, it's important to consider whether the events are independent or dependent on one another. An event is independent of other events in the sample space if the outcome of that event is not affected by the outcome of other events in the sample space.

For example, imagine a bag of ten sox, with five blue and five red. Without looking, you reach into the bag and draw out a red sox. Then you put the sox back in the bag and draw a blue one. The probability of drawing a red sox first is 5/10, or 50%. The probability that the second sox will be blue is also 5/10, or 50%. Because you put the first sox back, the probability of drawing the second sox is independent of the first. Neither event affects the other.

1. Probability of drawing and replacing a red sox
   - P(red) = 1/2 
2. Probability of drawing and replacing a blue sox after drawing and replacing the red sox:
   - P(red) = P(blue) = 1/2
3. Probability of drawing a red sox and then a blue sox:
   - P(red ∩ blue) = P(red) * P(blue) = (1/2) * (1/2) = 1/4

# When the probability of event B changes based on the outcome of event A, the probability of event B is said to be dependent on, or conditional on, event A

1. If the first sox was blue, then the probability of drawing a red sox the second time is 5/9 (because one blue is missing from the bag). Or "the probability of red given blue"
   - P(red | blue) = 5/9
 
2. If the first sox was blue, then the probability of drawing a blue sox the second time is 4/9 (because one blue sox is missing from the bag).
   - P(blue | blue) = 4/9

# The probability of two conditional events can be calculated by multiplying the probability of event A by the probability of event B conditioned on A.
  - P(A ∩ B) = P(A) * P(B | A)

1. Probability of drawing two blue marbles in a row without replacement:
   - P(blue) * P(blue | blue) = (1/2) * (4/9) = 2/9

2. robability of drawing a red marble and then a blue marble without replacement:
   - P(red) * P(blue | red) = (1/2) * (5/9) = 5/18

# Bayes's rule and conditional probability

 When we read in the news that a test is 99% accurate. It's not the probability that you are infected with a virus. It's the probability that you're infected given the condition that you get a positive corona test.
 
 1. Bayes's rule
    - probability of A given B equals the probability of B given A, times the probability of A, divided by the probability of B
    - P(A | B) = P(B | A) * P(A) / P(B) or, 

    - the probability of B where A~ is the inverse of A—so in this case, not being infected. The numerator is the scenario of interest, while the denominator represents the realm of scenarios that could give the condition.
    - P(A | B) = P(B | A) * P(A) / [P(A)*P(B|A) + P(A~)*P(B|A~)]
    - P(Infected| Positive Test) = P(Positive Test| Infected) * P(Infected) / P(Positive Test)

= .9999 * .000001/(.000001*.9999 + .999999*.0001) = .0099 or .99%

So that says that there's less than a 1% chance that you're really infected
