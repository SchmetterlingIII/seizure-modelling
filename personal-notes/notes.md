This file will contain notes from within the `model-development-log.ipynb` that explores the more technical aspects of the project.

# Abstraction Approaches
These are the initial ideas that I had for the developement of this model:
- Agent-based model (ABM) of neurotransmitters between pre- and post- synaptic nerves (connecting axon terminals to dendrites) to see how differences in concentrations of glutamate and GABA ($\gamma$-aminobutryate acid) affects the action potetials and global likelihood for excitation in neurons. *This would be close-up and hyper-local; the outputted probability from this could then be the input for a grid graph that could be rendered in a similar way to Bernoucilli percolation.*

- A more global design where the network has naturally, randomly occurring electrical impulses that propagates through the network (indicated by a highlighted node). The control variables are the E/I balance (and later mutations within certain cells) so that the global patterns are showed in this model.

# Open Questions

# Literature Sources
- `The emergence  of abnormal hypersynchronization in the anatomical structural network of human brain`: https://web.ece.ucsb.edu/Faculty/li/Paper7-NeuroImage-2013.pdf
- 
# Epilepsy-Alzheimer's Link
In looking for hypersynchronisation in the brain (https://academic.oup.com/brain/article/142/12/3936/5601465), I found that hypersynchronisation was also an important factor in the development of Alzheimer's in the brain. Amyloid-$\beta$ plaques in the brain cause an E/I imbalance, this causes neurotoxicity and neuronal death (similar to *status epilepticus*) and promotes cognitive decline, manifesting in symptoms of dementia such as memory loss, hallucinations and reduced agency (depending on the specific type). All research trying to find and model hypersynchronisation in the brain uses goal as the precursor to diagnosing Alzheimer's which is quite fascinating: as the synchronisation precedes the development of the stated amyloid-$\beta$ (A$\beta$) plaques and the gradual disruption of the neural circuitry.

Then I saw that there was a link between seizures (epilepsy) to dementia (https://www.alzheimers.org.uk/blog/what-link-between-seizures-and-dementia; https://pmc.ncbi.nlm.nih.gov/articles/PMC9352925/pdf/fneur-13-922535.pdf) it demonstrated a further necessity for these tools since having a somewhat unified model for this could interest reseachers into some topic for this.

There is a bi-directional relationship between Alzheimer's disease and seizures (doi.org/10.3389/fneur.2022.922535) and I understand this risk: epilepsy and seizures can develop through the A$\beta$ plaque deposits in the brain, which reinforces the cognitive decline shown in Alzheimer's. Although this surface-level relationship is trivial, I am interested that - in Alzheimer's and aging cells more generally - there is reduced neuronal excitability (doi.org/10.3389/neuro.24.002.2010) (does this mean reduced GABA concentrations? what specifically causes this mechanism to occur?) and so what is the relationship and what are ways of mitigating this network level degradation.

An idea that I wish to explore:
- As our cells age, is there there an increased susceptibility to global, network syncrhonisation since the mechanism to recognise localised triggers are weakened? What is even this mechanism initially? 
- Is there always a likelihood of this occurring (in an entirely "healthy" system), just with a near-zero probability?


# Heterogeneity (Session II)
**Task**: I need to find more comprehensive research on how neurons in the brain are heterogenous and how this could effectively be abstracted to a model that is still somewhat true to life. I would like to code out the E/I balance in the brain as well as finding other things that inform this process. 

One approach: Understanding how action potential actually propagate along neurons (i.e. how the dendrite "understands" which concentration of excitatory neurotransmitters is sufficient to activate the neuron at the axon hillock) and informing this probability (likely stored as some sort of `NumPy` matrix for easy handling) to activate cells. Then, adjustments to concentrations of E/I globally could take place. 
Leading on from this, applying some function that would cause mutations within edges **and** neurons randomly could see how, if only one edge has a high glutamate/low GABA concentration, neuronal misfiring can occur from this top down level.
This seems like the best approach for applying heterogeneity and now I will be conducting research on this to ensure that this is roughly the correct area. 

## Research
- How action potentials propagate along neurons (how is this information coded along the cells?)
- How to interpret/represent this information
- What other factors are the reasons for the hetergeneity of neurons?
- How to code probabilities with the concentration of glutamate/GABA?
- `Hodgkin-Huxley Model` (and try to understand their functioning since, on a local level, this would be helpful to understand propagation)
- Other models (came across the `Izhikevich Neuron Model` and I will try to code this out to understand its mechanisms - given that existing things have been created by researchers, it is better to leverage them. If all models are *theoretically* better than what I wish to do (which it seems like it), I will focus on the research into hypersynchronocity and develop an educational tool for this hyperspecific point of research).
  - https://hub.2i2c.mybinder.org/user/brian-team-brian2-binder-ul8m9sx2/notebooks/demo.ipynb
  - https://share.google/crnJu9E7H59CAJPQi
 
*This was all effectively done by reading the documentation on `Brian2`, now I will be testing out the code of this software with the goal of data collection.*








