# Notes
*This file will contain notes from within the `model-development-log.ipynb` that explores the more technical aspects of the project.*

----
# Abstraction Approaches
These are the initial ideas that I had for the developement of this model:
- Agent-based model (ABM) of neurotransmitters between pre- and post- synaptic nerves (connecting axon terminals to dendrites) to see how differences in concentrations of glutamate and GABA ($\gamma$-aminobutryate acid) affects the action potetials and global likelihood for excitation in neurons. *This would be close-up and hyper-local; the outputted probability from this could then be the input for a grid graph that could be rendered in a similar way to Bernoucilli percolation.*

- A more global design where the network has naturally, randomly occurring electrical impulses that propagates through the network (indicated by a highlighted node). The control variables are the E/I balance (and later mutations within certain cells) so that the global patterns are showed in this model.

# Open Questions

# Literature Sources
- `The emergence  of abnormal hypersynchronization in the anatomical structural network of human brain`: https://web.ece.ucsb.edu/Faculty/li/Paper7-NeuroImage-2013.pdf
- 
### Epilepsy-Alzheimer's Link
In looking for hypersynchronisation in the brain (https://academic.oup.com/brain/article/142/12/3936/5601465) I found one example of the understanding how hypersynchronicity in the brain emerges since it is important for many neuropathologies. Then I saw that there was a link between seizures (epilepsy as well) to dementia (https://www.alzheimers.org.uk/blog/what-link-between-seizures-and-dementia; https://pmc.ncbi.nlm.nih.gov/articles/PMC9352925/pdf/fneur-13-922535.pdf) it demonstrated a further necessity for these tools since having a somewhat unified model for this could interest reseachers into some topic for this.

Notes on Alzheimers:
Amyloid-$\beta$ plaques in the brain cause an E/I imbalance, this causes neurotoxicity and neuronal death (similar to *status epilepticus*) and is a fascinating unifying point - abstracted models may have a top-down view on things that can help with the collaboraton of topics by other researchers.

All research trying to find and model hypersynchronisation in the brain uses this idea as the precursor to Alzheimer's which is quite fascinating: this precedes the development of the stated amyloid-$\beta$ (A$\beta$) plaques and the gradual disruption of the neural circuitry.

My "theory" is that, as our cells age, there is an increased susceptibility to this syncrhonisation since the mechanism to recognise localised triggers are weakened? Or maybe there is always a likelihood of this occurring but in healthy neurons, this can be regulated easier and the probability is much lower. I need to find sources on this idea and try to link this to the model (and what stage of it this shoudl be integrated within)


# Heterogeneity (Session II)
**Task**: I need to find more comprehensive research on how neurons in the brain are heterogenous and how this could effectively be abstracted to a model that is still somewhat true to life. I would like to code out the E/I balance in the brain as well as finding other things that inform this process. 

One approach: Understanding how action potential actually propagate along neurons (i.e. how the dendrite "understands" which concentration of excitatory neurotransmitters is sufficient to activate the neuron at the axon hillock) and informing this probability (likely stored as some sort of `NumPy` matrix for easy handling) to activate cells. Then, adjustments to concentrations of E/I globally could take place. 
Leading on from this, applying some function that would cause mutations within edges **and** neurons randomly could see how, if only one edge has a high glutamate/low GABA concentration, neuronal misfiring can occur from this top down level.
This seems like the best approach for applying heterogeneity and now I will be conducting research on this to ensure that this is roughly the correct area. 

## Research





