# Modeling the Reliability of Ball Bearings

## Project Overview
This project applies **Multiple Linear Regression** and **Hypothesis Testing (F-Tests)** to model the fatigue life of deep-groove ball bearings. The analysis tests the validity of the theoretical model and the key industry assumption of a fatigue-life exponent `p = 3`, using classic data from Lieblein and Zelen (1956).

## Key Objectives
- Test if the fatigue-life model parameters are consistent across different bearing manufacturers.
- Validate the historical assumption that the load-life exponent `p = 3`.
- Perform a detailed analysis on the bearing types from a single manufacturer (Company B).

## Methodology
- **Model:** Generalized Fatigue-Life Model: $$`L = (fZ^a D^b / P)^p`$$
- **Linearization:** Transformed to a log-linear regression model: `ln(L) = α + β₁ln(Z) + β₂ln(D) + β₃ln(P)`
- **Statistical Technique:** Nested F-Tests for comparing regression models and testing hypotheses about parameter equality.
- **Tools:** Analysis was performed using R (or Python/other - specify what you used).

## Hypotheses Tested
1.  **H(a):** Parameter equality across different companies.
2.  **H(b):** Equality of the load exponent (`β₃`) across companies.
3.  **H(c):** Parameter equality across different bearing types within Company B.
4.  **H(d):** Equality of the load exponent (`β₃`) across types in Company B.
5.  **H(e):** Specific test for `p = 3` in Company B's bearing types.

## Results & Conclusions
- The full set of parameters **is not consistent** across different companies (Rejected H(a)).
- However, the critical load-life exponent `β₃` **is consistent** across companies (Failed to reject H(b)).
- For a single manufacturer (Company B), the load-life exponent `p` was **not statistically different from the theoretical value of 3** (Failed to reject H(e)).

## Files in this Repository
- `statPROJECT2ndSEM.pdf` - The full project report detailing the problem, methodology, and results.
- `bearing_data.csv` - [If you have it] The dataset used for the analysis.

## Technologies Used
R, RStudio, Linear Regression, Hypothesis Testing, Git
