# Ising-spin-networks

This repository contains materials related to the article *G. Czelusta, J. Mielczarek, **Quantum circuits for the Ising spin networks***.

* **tutorial.ipynb** introduce methods given in article
* **results.ipynb** contains results of simulations presented in the article
* **classical_results.ipynb** contains computations of spin networks states using tensor networks, in order to compare with ones obtained from quantum methods

The files **cost_history_*network*.csv** contain the histories of the cost function during optimisation, for 10 runs with random initial parameters.

The **params_last_*network*** folders contain files with the last parameters for each optimisation run.

In the **params_best_*network*** folders there are saved files with the best parameters for each optimisation run. Best parameter means that for this parameter the cost function had the smallest value during optimisation. Note: Due to statistical noise these are not necessarily the best "true" parameters.

The file **deka.csv** contains non-zero elements of the state vector for the dekagram.

In Loop Quantum Gravity (LQG), the states of the quantum geometry are represented by spin networks. These are graphs with links labelled by spin numbers. The nodes correspond to volume quanta (in the case of four-valent networks, tetrahedra) and the links represent the connectivity between them.

We can construct the state of the spin network by preparing a pair of spins for each link and then applying the Gauss constraint in each node.

In this article we present this construction on a quantum processor. We introduce operator $\hat{W}$ which can be used to apply Gauss constraint. The obtained state is transferred to an ansatz. The state can be represented in the form of ansatz parameters and can be easily reconstructed for further purposes.

We also introduce a method of gluing smaller spin networks to obtain larger ones. This method uses fewer qubits than building from scratch.