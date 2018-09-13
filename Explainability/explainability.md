footer: @JulioBarros http://E-String.com
slidenumbers: true
autoscale: true
build-lists: true
theme: Plain Jane

# Intro to Explainability in ML

## PDX ML

### Julio Barros

--- 
# Me:

* @JulioBarros 
* Machine Learning Engineer (Consultant)
* E-String.com

---

# Explainability


The idea of how well a human can understand the decision is often called _interpretability_ or _explainability_.

^ Lately there has been a lot of intereset in explainable AI/ML.

^ Nobody wants to feel discriminated against by an algorithm and when we don't like it's prediction or decision we want to know why it made that decision.

^ To manage social interaction: to create a shared meaning of something, and to change others’ beliefs & impressions, their emotions, or to influence their actions.

^ It is important to note though that this definition of explainability is still not very precise and open to interpretation.

---

# Confession

## I pulled a bait and switch.

---

# Explainability/Interpretability related to:

* Fairness - (socially) unbiased and not discriminating 
* Safety / Reliability - errors are not catastrophic
* Privacy - protecting sensitive information
* Justification - why a decision is good

^ sensitivity analysis

---

# You might be asked: _What_

What features were used to make this prediction/decision?

* Feature selection and engineering
* Model selection

---

# Or maybe: _How_

* How does the algorithm work?
* How does the input affect the output?
* How are features and outputs correlated?

^ Multiplies inputs by weights and passes them through a sigmoid ... not satisfying

---

# But _Why_ is special

Why was this prediction made?

**Why should I trust your prediction?**

^ * Why was I denied a loan?
^ To find meaning: to reconcile the contradictions or inconsistencies between elements of our knowledge structures.

---

# Good (understandable?) explanations

Deep down your boss/client/user wants the explanation to be:
- monotonic
- homoscedastic
- not probabilistic
- contrastive
- selective
- perscriptive
- conformant to social expectations


^ why p happend instead of q
^ what can I change to get what I want
^ only a few factors selected according to human biases
^ level/detail
^ increase in x always causes an increase in y
^ explanation approximately correct accross entire range

--- 

# Almost everyone

![inline](img/explanations.jpg)

--- 

# Radical Thesis

Explainability and interpretability are two different things.

* Explainability is _why_
* Interpretability is _how_

^ (human, post-hoc)
^ (transparency)

---
# Unfortunately

Humans want meaning (_why_). 

Explainability is understanding the _why_ (causation).

DS/ML deals in correlations.

Interpretability is understanding the _how_ (correlations).

### Correlation is not Causation.


---

# Example

![inline,80%](img/simple_linear.png)

^ X and Y are correlated.

^ X does not _cause_ Y.

^ How would you explain this model if:

^ - X were income and Y were credit limit?
^ - X was the time a rooster crowed and Y was the sunrise?



---

# So, what can we do?

---

# Well ...

- Run randomized control trials (?)
- Build structural/causal models (?)
- Understand the correlations the best we can ...

---

# Great power / responsibility

Keep in mind the human (mind's) tendencies to:

- want causation
- want to compare and contrast 
- want _perscriptive_ insight

---

# Understanding the correlations in our models

| Approach | Tool | Area |
|---|---|---|
| Linear models | coefficients | global |
| Decision trees / Rules | nodes | global |
| |||
| Tree ensemble | feature importance | global |
| Feature exploration | permutation importance  | global |
| | Partial Dependence Plot (PDP) | single feature* / global |
| | Indiv. Cond. Expectation (ICE) | single feature / subsample |
| |||
| Surrogate Models | Local Inter. Model-agnostic Exp. (LIME) | multi feature / local |
| | Shapley values | multi feature / local |

^ sometimes called proxies

--- 

# Data: King County Washington home sales

* May 2014 and May 2015
* Kaggle https://www.kaggle.com/harlfoxem/housesalesprediction
* 19 features
* 21,613 observations

---
# Features

|||
|---|---|
| id - a notation for a house|  date - Date house was sold |
| price - Price is prediction target | bedrooms - Number of Bedrooms/House |
| bathrooms - Number of bathrooms/bedrooms | sqft_living - square footage of the home |
| sqft_lot - square footage of the lot | floors - Total floors (levels) in house |
| waterfront - House which has a view to a waterfront | view - Has been viewed |
| condition - How good the condition is ( Overall ) | grade - overall grade given to the housing unit, based on King County grading system |
| sqft_above - square footage of house apart from basement | sqft_basement - square footage of the basement |
| yr_built - Built Year | yr_renovated - Year when house was renovated |
| zipcode - zip | lat - Latitude coordinate |
| long - Longitude coordinate | sqft_living - 15Living room area in 2015(implies-- some renovations) This might or might not have affected the lotsize area |
| sqft_lot15 - lotSize area in 2015(implies-- some renovations) |  |

--- 
# King County

![inline](img/king_county_map.png)

---

# Switch to notebook

---

# Summary

- Explainability vs Interpretability
- Feature permutation - Eli5
- Partial Dependece Plot - pdpbox
- Shapley - shap
- IML for R

---

# Resources

[A Survey Of Methods For Explaining Black Box Models](https://arxiv.org/abs/1802.01933v3)
[Explanation in Artificial Intelligence](https://arxiv.org/abs/1706.07269)
[Consistent Individualized Feature Attribution for Tree Ensembles](https://arxiv.org/abs/1802.03888)
https://christophm.github.io/interpretable-ml-book/

https://github.com/SauceCat/PDPbox
https://github.com/TeamHG-Memex/eli5
https://github.com/marcotcr/lime
https://github.com/slundberg/shap

https://www.kaggle.com/harlfoxem/housesalesprediction

---

# Thank You!

#### @JulioBarros / E-String.com /  Julio@E-String.com

## Questions?
