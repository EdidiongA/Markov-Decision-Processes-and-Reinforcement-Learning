# Reinforcement Learning and Markov Decision Processes

![Python](https://img.shields.io/badge/Python-3.x-3776AB?logo=python&logoColor=white)
![Gymnasium](https://img.shields.io/badge/Gymnasium-Frozen%20Lake-0081A5)
![bettermdptools](https://img.shields.io/badge/bettermdptools-PI%20%7C%20VI%20%7C%20Q--learning-4B8BBE)
![Jupyter](https://img.shields.io/badge/Jupyter-notebooks-F37626?logo=jupyter&logoColor=white)
![Course](https://img.shields.io/badge/Georgia%20Tech-CS%207641%20Machine%20Learning-B3A369)

Policy iteration, value iteration and Q-learning applied to two Markov Decision Processes of contrasting size: Frozen Lake with 100 states and the Gambler's Problem with 500 states. The study compares how the three algorithms converge, what policies they find, and how their wall-clock cost scales with the state space.

Built for CS 7641 Machine Learning at Georgia Tech.

---

## Contents

- [Overview](#overview)
- [The two problems](#the-two-problems)
- [Algorithms](#algorithms)
- [Project description](#project-description)
- [Getting started](#getting-started)
- [Repository structure](#repository-structure)
- [What each notebook covers](#what-each-notebook-covers)
- [References](#references)
- [Author](#author)
- [License](#license)

---

## Overview

| | |
|---|---|
| **Problems** | Frozen Lake (100 states, 10x10 map) and the Gambler's Problem (500 states) |
| **Algorithms** | Policy iteration, value iteration (dynamic programming) and Q-learning (model-free reinforcement learning) |
| **Frameworks** | Gymnasium (OpenAI Gym) environments and the bettermdptools solvers |
| **Analysis** | Policy and value visualisation, convergence behaviour, and wall-clock execution time for each algorithm on each problem |
| **Format** | Four Jupyter notebooks |

## The two problems

| Problem | States | Nature | Why it was chosen |
|---|---|---|---|
| Frozen Lake | 100 (10x10 grid) | Stochastic grid world: reach the goal without falling through holes on slippery ice | A small, visual MDP where the learned policy can be drawn and inspected |
| Gambler's Problem | 500 | A gambler bets on coin flips to reach a target capital; states are the current capital | A large, non-spatial MDP that stresses how the algorithms scale |

## Algorithms

| Algorithm | Type | Needs the transition model? |
|---|---|---|
| Policy iteration | Dynamic programming | Yes |
| Value iteration | Dynamic programming | Yes |
| Q-learning | Model-free reinforcement learning | No; learns from experience |

Running all three on both problems lets the model-based and model-free approaches be compared directly on the same MDPs, including the execution-time cost of each.

## Project description

This project examines two Markov Decision Process (MDP) problems – the Frozen Lake Problem and the Gambler’s Problem using [OpenAI gym](https://gymnasium.farama.org/) and [bettermdptools](https://github.com/jlm429/bettermdptools) which are reinforcement learning algorithms or frameworks. The Frozen Lake Problem is implemented with a small number of states (100 states) and the Gambler’s Problem is implemented with a large number of states (500 states). Policy and value iteration algorithms are run on these two MDP problems. Subsequently, the Q-Learning algorithm, a reinforcement learning algorithm, is run on these two MDP problems.

## Getting started

### Requirements

Python 3.8 or later and Jupyter.

```bash
pip install numpy matplotlib seaborn gymnasium bettermdptools jupyter
```

`bettermdptools` supplies the planning and learning solvers and the plotting helpers; `gymnasium` supplies the Frozen Lake environment.

### Run the notebooks

```bash
jupyter notebook
```

Open the notebooks in the order listed below and run each top to bottom.

## Repository structure

```
.
├── README.md
├── Markov_Decision_Processes_and_Reinforcement_Learning.ipynb           # Frozen Lake: environment, PI, VI, Q-learning
├── Markov_Decision_Processes_and_Reinforcement_Learning_part1b.ipynb    # Frozen Lake: policy evaluation and wall-clock timing
├── Markov_Decision_Processes_and_Reinforcement_Learning_part2.ipynb     # Gambler's Problem: environment, PI, VI, Q-learning, timing
└── Markov_Decision_Processes_and_Reinforcement_Learning_part2b.ipynb    # Gambler's Problem: states, actions and rewards display
```

## What each notebook covers

| Notebook | Problem | Contents |
|---|---|---|
| `..._Learning.ipynb` | Frozen Lake, 100 states | Visualises the 10x10 map before any algorithm runs, evaluates policy types, then runs policy iteration, value iteration and Q-learning |
| `..._part1b.ipynb` | Frozen Lake, 100 states | Policy evaluation, the three algorithms, and a comparison of wall-clock times |
| `..._part2.ipynb` | Gambler's Problem, 500 states | Implements the environment, runs policy iteration, value iteration and Q-learning, and measures execution times |
| `..._part2b.ipynb` | Gambler's Problem, 500 states | Displays the states, actions and rewards of the MDP |

## References

- Sutton, R. S. and Barto, A. G. (2018). *Reinforcement Learning: An Introduction*, 2nd edition. MIT Press. The Gambler's Problem is Example 4.3.
- Farama Foundation. Gymnasium: Frozen Lake environment. [Documentation](https://gymnasium.farama.org/)
- Mansfield, J. bettermdptools. [GitHub](https://github.com/jlm429/bettermdptools)

## Author

**Edidiong-Abasi Anwanane**  
MSc Computer Science, Georgia Institute of Technology  
[Portfolio](https://edidionga.github.io) · [LinkedIn](https://www.linkedin.com/in/edidiong-abasi-anwanane/) · [GitHub](https://github.com/EdidiongA)

## License

MIT. See [LICENSE](LICENSE).
