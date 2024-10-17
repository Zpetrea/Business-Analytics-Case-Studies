# Business-Analytics-Case-Studies
This repository contains a Business Analytical Case Study and its findings. The findings are written as a 4-5 page paper with JMP snippets inserted within the paper.

We will construct predictive models to examine determinants of medical costs billed by health insurance companies. This information will be useful to eventually determine premiums.

# Below are the data variables:
## Age
: insurance contractor age, years
## Sex
: insurance contractor gender, [female, male]
## BMI
: Body mass index, providing an understanding of the body, weights that are relatively high or low relative to height, objective index of body weight (kg / m ^ 2) using the ratio of height to weight, ideally 18.5 to 24.9
## Children
: number of children covered by health insurance / Number of dependents
## Smoker
: smoking, [yes, no]
## Region
: the beneficiary’s residential area in the US, [northeast, southeast, southwest, northwest]
## Charges
: Individual medical costs billed by health insurance, $ (
predicted value)

# The models we will consider are:
- Boosted NN (NTanH(2), 500 boosts )
- Boosted NN (NTanH(2), robust, 500 boosts )- Note: robust option is similar to using Cauchy distribution in penalized regressions, it uses an estimation method (Laplacian likelihood function) that can produce better predictions if the outliers are important in thedata set.
- Boosted NN (NTanH(2), 500 boosts, learning rate=.05)- Note: this applies a smaller learning rate at each boosting, and hence, may take a bit longer, but potentially could improve results.
- OLS as the base method
As conducted with NN models and the validation column, as usual, use the random seed 123.
Identify the most important variables.

As a new case
, suppose you have 45 year old non-smoker male with a BMI of 38 from the southeast, who has 2 children. What is your predicted medical costs for him?
