---
layout: default
---

# Ryan Lindberg

Email: [rylindberg@ucsd.edu](mailto:rylindberg@ucsd.edu)  
Section: D10  
Mentors: Emily Belli, Jeff Candy, and Igor Sfiligoi

**What is the most interesting topic covered in your domain this quarter?**

The most interesting topic to me has been using neural networks to predict turbulent transport in a fusion plasma. Our models learn to approximate the outputs of TGLF, which calculates how turbulence moves heat and particles through the plasma. A trained network can make these predictions much faster, which is useful when many different plasma conditions need to be evaluated. I am especially interested in the limits of this approach. A model can perform well on familiar conditions but become unreliable when the inputs differ from its training data.

**Describe a potential investigation you would like to pursue for your Quarter 2 Project.**

I would like to investigate whether model uncertainty can help us choose more useful TGLF simulations for training. I would start with a small training set and use disagreement among several neural networks to select additional cases. I would compare this approach with randomly selecting cases at the same training sizes. Both methods would be evaluated on a fixed test set that is kept out of training and case selection. The main question would be whether uncertainty can help us reach a given prediction accuracy with fewer TGLF evaluations. I could first test the idea using a pool of existing simulation results, treating unselected outputs as unavailable. This would let me evaluate the approach before spending time generating new simulations.

**What is a potential change you'd make to the approach taken in your current Quarter 1 Project?**

I would add a test that holds out an entire radial location from the DIII-D training data. A random split can place similar plasma conditions in both the training and test sets, so it may not fully show how well the model handles a new region. Training on the remaining radii and evaluating on the excluded radius would give us another way to assess generalization. I would repeat this for several radii and report errors separately for ion heat flux, electron heat flux, and electron particle flux. I would also check whether disagreement among the networks increases when their predictions are less accurate.

**What other techniques would you be interested in using in your project?**

I would be interested in comparing our neural networks with gradient boosted trees on the same inputs and data splits. This would help determine whether the neural networks offer an advantage over another approach suited to tabular data. I would also like to try Gaussian process regression on a smaller dataset and compare its uncertainty estimates with the spread of predictions from our neural network ensemble. Finally, sensitivity analysis could help us understand which plasma inputs have the strongest effect on each predicted flux.
