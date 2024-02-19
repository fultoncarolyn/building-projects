# Georgraphic Spreading Project

## Initial Questions

1. What are the conditions/assumptions necessary for use?

2. How is the SIR model adjusted to incorporate the spacial component? (PDE?)

3. For our application, what do we care about?

4. What are the limitations of this approach?


## Resources

Spatial SIR Model (paper) -> my favorite/most interesting
<https://arxiv.org/pdf/2102.10145.pdf>

Regional Kinetics (paper) 
<https://www.ncbi.nlm.nih.gov/pmc/articles/PMC9483512/>

COVID 19 spread kernel modulated? (paper)
<https://www.pnas.org/doi/full/10.1073/pnas.2023321118>

SIR as a transport PDE problem (paper)
<https://www.sciencedirect.com/science/article/pii/S0895717710002906>


## Notes/Ideas

Is a baseline model required? Comparing to data for simulations - is data reliable/continuous?

- Structure of models, i.e. patches, come from structure of data since we recieve usually city based data

How to incorporate localized immunity?

- Each patch is SIR bubble which has dependency/coupling with neighboring patches. The coupling depends on what? distance, population center, etc?

Continuous vs discrete models... when is the later useful?

- Balance between continuous time vs discrete outputs (ex what happens for a thousandth of a person being infected? -> dynamics issues)

What is kernel-modulated, how is it useful? What other kinds of transforms/fancy math are out there and are there any worth exploring to incorporate renewal equation project?

- yeah no idea but that's okay read into it and maybe it will fit when assumptions change later? 


## From Stephen

Julia Gog <https://scholar.google.com/citations?user=0FZBXDYAAAAJ&hl=en>
- Influenza Spatial Transmission (metapopulation) <https://journals.plos.org/ploscompbiol/article/file?id=10.1371/journal.pcbi.1003635&type=printable>

Challenges (Steven Riley <https://scholar.google.com/citations?user=1mTtPIIAAAAJ&hl=en>)
- 2015 <https://www.sciencedirect.com/science/article/pii/S1755436514000310?via%3Dihub>
- 2007 <https://www.science.org/doi/10.1126/science.1134695>

Metapopulation Dynamics (Ilkka Hanski)
- <https://www.nature.com/articles/23876>
- <https://books.google.com/books?hl=en&lr=&id=jsk4Nt_8X8sC&oi=fnd&pg=PA1&ots=gEWi5qEX2G&sig=rvJCwgcDPsACuCbSU8O_cjwWTKc#v=onepage&q&f=false>


### Follow up questions/ideas

**Goal:** Construct model with coupling terms between "nodes" which are subpopulations/communities. Each node has it's own SIR "state" which relates to the transmission between nodes.

Metapopulation will be the key to describe these relationships (nested populations of sorts).

Coupling terms will likely be a probability of interaction between nodes based on spatial which then has a likelihood of resulting in infection that should also depend on the state of the nodes at point of contact.
- If there's randomness involved in modeling these things then how do we provide an answer if each outcome may be slightly different?

Probabalistic over all simulations (math def) -> statistic from outcomes and all that fun stuff

## Coding help
Simple example(s) to walk through and get used to R <https://rpubs.com/choisy/sir>

- Are the functions reliable or should we code up processes (ex RK4) for any reason? Makes sense to start by doing that for proof of concept...

no random number generator - probability of s to i r etc (stay away from packages for now to learn the science! Does solving ODE really help no)