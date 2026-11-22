# Feature Engineering

Feature engineering means preparing the columns in a dataset or creating new ones so a machine learning model can learn useful patterns more easily.

For example, if we want to predict house prices and we know the year each house was built, we can use that year to calculate the **age of the house**.

## Types of Feature Engineering

### 1. Feature Transformation

We change how an existing feature is shown or used.

- **Missing value imputation** means filling in missing values. For example, we can fill missing house sizes with the median size from the training data.
- **Handling categorical features** means converting categories into a format the model can use. For example, we can create an `is_apartment` column with `1` for apartments and `0` for other homes.
- **Outlier detection and handling** means finding unusual values and checking what to do with them. For example, a negative house size is probably a data entry error, while a very large house could be real.
- **Feature scaling** means putting numbers on a similar scale. This helps models like K-nearest neighbors when one column has much larger numbers than another.

### 2. Feature Construction

We make a new feature using information we already have. For example, we can subtract `year_built` from `year_sold` to create `house_age_at_sale`.

### 3. Feature Selection

We choose which existing features to keep. For example, if house size is given in both square feet and square meters, we can keep just one because both columns give us the same information.

### 4. Feature Extraction

We turn data such as text or images into features a model can use. For example, we can turn a house description into numbers that show how important words like “balcony” or “parking” are in that description. One method for doing this is **TF-IDF**.