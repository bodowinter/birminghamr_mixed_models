# birminghamr_mixed_models
# Mixed Poisson regression analysis with crossed random effects

We'll use this markdown file for the hands-on session. The data is taken from Korean dyadic interactions in two conditions:

- A) speaking with a friend
- B) speaking with a professor

The model we'll fit estimates the count of honorifics for both of these conditions, with the expectation that speakers will use more honorifics when speaking with the professor. A mixed model is needed because there are repeated samples per participant as well as repeated samples per item. This mixed model will be a mixed Poisson regression model because the main response variable is a count variable.

The two random effects (subject and item) will be crossed. That is, each participant saw each item. Experimental designs with crossed random effects structures are very common in experimental psychology and psycholinguistics, but the analysis pipeline can also be adapted to implement models with hierarchical random effects structures (e.g., pupil within class within school within district).

The script implements the mixed Poisson regression first with lme4 and then shows how likelihood ratio tests can easily be performed with the afex package. The model is then implemented in a Bayesian fashion with brms.

The following packages are needed to run the script:

- tidyverse
- lme4
- afex
- brms
