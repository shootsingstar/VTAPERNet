## Overview

This directory contains the `PR-vector` files `PR_740.csv` and `PR_61.csv`, which represent the dimensionality reduction results used during the training of the model. These files were generated using UMAP, a technique that involves some level of randomness in its process.

## Important Note

The results in `PR_740.csv` and `PR_61.csv` were specifically used to train this model. Because UMAP includes random initialization and random neighbor search, running UMAP again might produce different results even with the same data. This can lead to discrepancies between the training and prediction phases, potentially degrading the performance of the model.

### Using the Trained Model

If you plan to use the trained model for making predictions:

1. **Do not overwrite** the `PR_740.csv` and `PR_61.csv` files with new dimensionality reduction results.
2. Ensure that the input data for predictions aligns with the dimensionality reduction performed during training.

### Recommendation

If you need to apply dimensionality reduction to new data for prediction purposes, it is crucial to:

- Use the same UMAP configuration (including the random seed) as was used during training.
- Alternatively, you can use the existing reduced data from `PR_740.csv` and `PR_61.csv` to maintain consistency.

By following these guidelines, you can ensure that the model's predictions are consistent and reliable.