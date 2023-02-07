# SQA Undergraduate Research Scholarship Research Summary

In this research, I was tasked with determining the usage of quantum Monte
Carlo method found in [Ryan O'Donnell's
paper](https://arxiv.org/pdf/2208.07544.pdf) and his [presentation](https://www.youtube.com/watch?v=W3aLlgrINxE).

In the following sections I will go through a summary of the topics that I
explored, where I found uses, where I was stuck and any future paths that I
found.

I will also include links to any papers and articles that I found useful

## Financial Application
During my research, I found applications in finance is the easiest due to the number of derivatives that utilised Monte Carlo method already.
However, I did not look at how a quantum algorithm may be modified to better accommodate creating the paths that a
derivatives may take over time (i.e. the price vs time of a derivative) and just assumed that they can be generated.

Here are applications in Finance include:
- Pricing Path-Independent Options (e.g. European Call and Put Option)
  - [Option Pricing using Quantum Computers](https://arxiv.org/pdf/1905.02666.pdf)
    - Utilises amplitude estimation to price path-independent, multi-asset and path-dependent option.
- Pricing Path-Dependent Options (e.g. Asian Options)
  - [A Threshold for Quantum Advantage in Derivative Pricing](https://arxiv.org/pdf/2012.03819.pdf)
    - There are parts on path generation and error analysis that I didn't understand that may benefit from quantum access
  - [Quantum computational finance: Monte Carlo pricing of financial derivatives](https://journals.aps.org/pra/abstract/10.1103/PhysRevA.98.022321)
    - This provides a good explanation of Black-Scholes-Merton model and how it can be used to price options
    - Personally couldn't understand the quantum algorithms used but includes pricing of Asian Options and error analysis.
- Determining Value-At-Risk (VaR) and Conditional Value-At-Risk (CVaR)
  - [Efficient Monte Carlo methods for value-at-risk](https://www0.gsb.columbia.edu/faculty/pglasserman/Other/masteringrisk.pdf)
    - This paper provides an explanation on Monte Carlo Method as well as a comparison between common methods to estimate VaR.
  - [Credit Risk Analysis using Quantum Comouters](https://arxiv.org/pdf/1907.03044.pdf)
    - Goes through a quantum algorithm (didn't understand this lol) that allows for the estimation of VaR;

These papers are not specifically linked to Monte Carlo method or related to what I found in my research but may be worth a read.
- [A Survey of Quantum Computing for Finance](https://arxiv.org/pdf/2201.02773.pdf)
  - Provides an extensive list of applications
- [Towards Pricing Financial Derivatives with an IBM Quantum Computer](https://arxiv.org/pdf/1904.05803.pdf)
  - More on the math behind pricing assets and how quantum circuits can be created for the purpose of quantum computing.
- [Quantum computing for finance: Overview and Prospects](https://www.sciencedirect.com/science/article/pii/S2405428318300571?via%3Dihub#bib001)
    - Goes through a few more methods that quantum computing can be used in finance that are not limited to Monte Carlo.

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
  - For example, in [Hamoudi's PhD](https://yassine-hamoudi.github.io/files/other/PhDthesis.pdf), he was able to determine that a quantum algorithm could lead to saving in terms of space relative to a classical algorithm when determing frequency moments for a stream.
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
    - [Quantum Speedup of Monte Carlo Methods](https://royalsocietypublishing.org/doi/10.1098/rspa.2015.0301#d3e10400) means partition functions.- Distinguishing Classical Probability Distributions

- Determining Probability Distributions
  - [Quantum Algorithms for Distribution-Free Junta Testing](https://link.springer.com/chapter/10.1007/978-3-030-19955-5_5)
  - I couldn't understand the math pass what Hellinger Distance is defined to be and the O'Donnell's paper provided a good and concise use for it, so I didn't go any deeper.
  - There may be more applications hidden within determining distribution, but I am not too sure.

- Other suggestions from papers
  - [Near-Optimal Quantum Algorithms for Multivariate Mean Estimation](https://dl.acm.org/doi/pdf/10.1145/3519935.3520045)
    - Provides some suggestions on applications tho I didn't really understand any of them.