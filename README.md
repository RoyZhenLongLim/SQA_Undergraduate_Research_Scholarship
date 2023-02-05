# SQA Undergraduate Research Scholarship Research Summary

In this research, I was tasked with determining the usage of quantum Monte
Carlo method found in [Ryan O'Donnell's
paper](https://arxiv.org/pdf/2208.07544.pdf).

In the following sections I will go through a summary of the topics that I
explored, where I found uses, where I was stuck and any future paths that I
found.

## Financial Application
Applications in Finance include:
- Pricing Path-Independent Options (e.g. European Call and Put Option)
- Pricing Path-Dependent Options (e.g. Asian Options)
- Determining Value-At-Risk (VaR) and Conditional Value-At-Risk

Here are the documents on interest:
- 

## Property Testing Algorithms
This is a good lead for more.
- Proximity-Oblivious Testers (POTs) can be improved if they utilised random sampling (depends on how they work)
  - Found a specific example that solved the problem of determine if a bit string was sorted (this one example had a proof that I could understand)
  - There are potentially more applications in the additional exercises in the lecture notes that I couldn't prove.
- The lecture notes from [Tel-Aviv University](https://www.wisdom.weizmann.ac.il/~oded/PDF/dana-tech.pdf) and [Weizmann Institute of Science](https://www.wisdom.weizmann.ac.il/~oded/PDF/dana-tech.pdf) are a good place to start.


## Data Streaming Algorithms
- Looked at these [lecture notes from Dartmouth College](https://www.cs.dartmouth.edu/~ac/Teach/data-streams-lecnotes.pdf)
- Didn't end up finding an application
  - Most of the algorithm didn't utilise random sampling
  - Instead, they utilise estimators that are tailored to problems, which made it hard to include Monte Carlo Method
- This topics likely has applications I didn't understand
  - For example, in [Hamoudi's PhD](https://yassine-hamoudi.github.io/files/other/PhDthesis.pdf), he was able to determine that quantum algorithm could lead to saving in terms of space.
  - I don't understand how the algorithm works in Section 9.4 in the PhD paper but it could potentially be improved using the algorithm in O'Donnell's paper.

## Randomized Algorithms
For randomized algorithms, I use the books:
- Randomized Algorithms by Rajeev Motwani & Prabhakar Raghavan
- Probability and Computing: Randomized Algorithms and Probabilistic Analysis by Micheal Mitzenmacher & Eli Upfal

I didn't find any applications here.
Specifically, there weren't any algorithm that utilise random sampling in order to determine means.
The randomized part of the algorithm usually came from a decision problem where the output is random (e.g. randomly choosing a pivot for Randomized QuickSort) instead of determining some quantity.

## Misc
This section includes any small tangents that I took during my research. 
They are generally quite small and I hit a dead end pretty quickly.

- Simulated Annealing
  - This is a method of determine an optimal solution by simulating metal cooling and something to do with minimising energy states.
  - I don't understand enough on this to provide a judgement on its usefulness.
- Markov Chain Monte Carlo (MCMC) Approximate Counting Algorithms
  - Didn't find any that utilise random sampling.
  - Don't think this is a good lead.
- Applications in Statistical Physics
  - An application for Statistical Physics is Monte Carlo Integration, where a quantity may be determined by sampling.
  - The [wikipedia article provides a summary](https://en.wikipedia.org/wiki/Monte_Carlo_method_in_statistical_physics)
  - I couldn't find a specific example of a quantity that utilised this tho when I went through the book Monte Carlo Simulation in Statistical Physics: An Introduction Fifth Addition by Kurt Binder and Dieter W.Heermann.
  - This is likely due to my lack of understanding rather than a lack of uses tho as I did find something called a partition function that seems to use monte carlo but couldn't understand what it meant or what it was used for.
- Distinguishing Classical Probability Distributions
  - [Quantum Algorithms for Distribution-Free Junta Testing](https://link.springer.com/chapter/10.1007/978-3-030-19955-5_5)
  - I couldn't understand the math pass what Hellinger Distance is defined to be and the O'Donnell's paper provided a good and concise use for it, so I didn't go any deeper.
  - There may be more applications hidden within determining distribution, but I am not too sure.
