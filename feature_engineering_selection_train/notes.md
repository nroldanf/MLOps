# Feature Engineering

- Use the same seed/random state to split the dataset. Review which else there is a random process so the random seed is set with the same values.
- If an imputation method like mode or mean imputation is used, save that value to make sure all intermediate pipeline states are reproducible.
- Persist frequent labels.
- Persist the scaler.
- Persist any mapping dictinary if there is __Binning__ for categorical/numerical variables
