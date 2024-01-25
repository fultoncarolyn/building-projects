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