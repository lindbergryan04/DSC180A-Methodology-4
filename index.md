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

I would like to investigate how newer neural network techniques, different architectures, and larger training datasets could improve our TGLF surrogate models. Our current simple ensemble appears competitive with results reported in the literature, which makes me interested in how much further we could improve it. I would compare different architectures under the same evaluation conditions and gradually increase the training dataset size to see how performance changes. We have the compute capabilities to generate our own TGLF datasets, and it appears that an expansive dataset with high attention to detail does not yet exist for this field of research. I would also measure computational cost to determine whether improvements in accuracy justify the additional resources.

**What is a potential change you'd make to the approach taken in your current Quarter 1 Project?**

I would explore using a neural network ensemble to estimate prediction uncertainty. One of my groupmates presented results from this approach in a meeting, and they looked promising. Using disagreement among independently trained networks seems worth comparing with our current approach of constructing a 90% prediction interval and adjusting it using prediction errors. I would test which method produces more reliable uncertainty estimates by checking how often the intervals contain the actual TGLF outputs and how wide those intervals are.

**What other techniques would you be interested in using in your project?**

I am interested in using small groups of AI agents to investigate different approaches at the same time. The agents could review research, implement candidate models, and compare results to help rule out weak approaches and identify promising directions. Recent research by OpenAI and collaborators used thousands of agents to identify new research leads in biological data. I could not work at that scale, but I think a smaller version could be useful for our project. Given the performance of our current models and the pace of improvement in AI tools, I would like to test whether this workflow helps us find useful improvements faster. I would still review the code and verify the results myself.
