# birminghamr_mixed_models
example of a mixed poisson regression analysis (korean dyad data)

We'll use this markdown file for the hands-on session. The data is taken from Korean dyadic interactions in two conditions:

- A) speaking with a friend
- B) speaking with a professor

The model we'll fit estimates the count of honorifics for both of these conditions, with the expectation that speakers will use more honorifics when speaking with the professor. A mixed model is needed because there are repeated samples per participant as well as repeated samples per item. This mixed model will be a mixed Poisson regression model because the main response variable is a count variable.

The script implements this model first with lme4 and then shows how likelihood ratio tests can easily be performed with the afex package. The model is then implemented in a Bayesian fashion with brms.

The following packages are needed to run the script:

- tidyverse
- lme4
- afex
- brms
