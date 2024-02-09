# Renewal Equations for Infectiousness Project

## Initial Questions

1. What domain/restrictions pertain to these functions? Is that something to really care about?

2. Does this structure require fitting to data or is it more of a theoretical approach (randomized delta)?

3. What are the limitations of this approach?

4. Are we going against the grain by doing this or are there suspicions out there about the common approach?


## Resources

On the renewal equation (paper) 
<https://arxiv.org/pdf/2006.16487.pdf>

Libre Stats (text)
<https://stats.libretexts.org/Bookshelves/Probability_Theory/Probability_Mathematical_Statistics_and_Stochastic_Processes_(Siegrist)/15%3A_Renewal_Processes/15.02%3A_Renewal_Equations>

Stochastic Models Columbia (lecture)
<https://www.columbia.edu/~ww2040/6711F12/lect1009.pdf>

Renewal equation model for contact tracing (talk)
<https://www.youtube.com/watch?v=a_VNNT9yyI0>


## Notes/Ideas

How does this relate to stochastic processes? I am seeing that a lot...

- Worth considering some background work here

What assumptions about the data/model do we need to make for this to work? ex Independent Identically Distributed

- Depends on data so starting with minimal assumptions for simplicity

How is this different from renewal theory in stats?

- Idk but that's not wroth pursuing most likely. Need to remain within application as we can

How does it relate to the reproduction number? Is that relevant/something we care to explore? <https://royalsocietypublishing.org/doi/10.1098/rsif.2021.0429>

- Yes, worth exploring more meaning of $R_0$ here and how this may be important/impactful as changing the infectious distributions would alter reproduction number

Heterogeniety vs homogeneity chages how this is used? When would we ever use the later?

- Yes, but individualization might not be productive or helpful. Again, start with minimal assumptions and build up.

When is the lower bound of our intergral $-\infty$ vs 0?

- Mathematically equivalent. Could confirm if you want to feel like a math nerd I guess

How can we produce the force of infection/what type of metrics do we care about? Individual infectiveness over time, vs age of population, etc

- YES super useful... what have other people done? what is too much to incorporate? 

Is overfitting an issue? How do we check for accuracy?

- Compare to simulated data which is dependent on assumptions


## From Stephen

Framework example in recent publication <https://www.science.org/doi/10.1126/science.abb6936#core-collateral-media>

Odo Deikmann <https://scholar.google.nl/citations?user=hpOJncQAAAAJ&hl=en>
- Dynamics of immune status <https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6280846/>
- Renewal eqns on Banach spaces <https://link.springer.com/chapter/10.1007/BFb0083485> (i fear these words)
- Renewal eqns and PDEs <https://arxiv.org/pdf/2201.05323.pdf> (for full book see <https://link.springer.com/book/10.1007/978-3-662-13159-6>)

### Follow up questions/ideas

Piecewise deterministic Markov Processes? Need to contextualize random variable and Markov things

REqns: the processes is an idealized stochastic model for events that occur randomly in time. The defining property of a renewal process—the fact that the process restarts at each arrival time, independently of the past. Key tools: measures, convolutions, and transforms. <https://www.randomservices.org/random/renewal/Equations.html>
