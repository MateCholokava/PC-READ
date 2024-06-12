# PC-READ (Principal Component Reconstruction Error based Anomaly Detection)
## Introduction
This project introduces PC-READ, a novel approach for unsupervised and semi-supervised anomaly detection. PC-READ leverages principal component analysis (PCA) to reconstruct data and identify discrepancies between the original and reconstructed data as potential anomalies.

## Data Considerations
- Unclean/Contaminated Data: PC-READ is designed to handle data with unknown contamination levels. If the nature or level of anomalies is known, you can apply denoising techniques or other preprocessing steps.
- Semi-Supervised Approach: When you have some labeled anomalies, you can enhance PC-READ by incorporating synthetic anomalies to improve model training and validation.
## Synthetic Anomaly Generation (Semi-Supervised)
The following techniques can be used to generate synthetic anomalies to balance your training data:
- ## SMOTE (Synthetic Minority Over-sampling Technique):
    - Creates synthetic samples by interpolating between existing anomalies and their nearest neighbors.
    - Advantages: Effective for imbalanced datasets.
    - Considerations: May not capture all types of anomalies.
- ## Noise insertion
    - Adds random noise (e.g., Gaussian) to normal data points.
    - Advantages: Simple and versatile.
    - Considerations: The type and level of noise should be carefully chosen.
- ## Random adjustment
    - Modifies a few features of normal data points by a random amount.
    - Advantages: Can create diverse anomalies.
    - Considerations: Set bounds to keep adjustments realistic.
- ## Horizontal and Vertical Flip
    - Advantages: Useful for orientation-sensitive anomalies.
    - Considerations: Only applicable to image data.
