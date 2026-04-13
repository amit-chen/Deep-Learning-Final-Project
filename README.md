# Deep-Learning-Final-Project

OverviewThis repository presents Deep-SSFS, an advanced extension of the original Self-supervised Spectral Feature Selection (SSFS) algorithm.
Our core contribution involves replacing the classical surrogate model (e.g., XGBoost) with a Deep Learning architecture (MLP).
This allows the model to learn more complex, non-linear relationships within high-dimensional spectral manifolds.

The project evaluates the model's ability to identify high-quality features in image data (MNIST and Fashion-MNIST) as sample sizes scale,
focusing on the "Data Hunger" phenomenon and the robustness of deep neural surrogates compared to tree-based baselines.

Key Features:
1. Deep Surrogate: Utilizes a Multi-Layer Perceptron (MLP) with a learnable selection layer (Lasso $L_1$ regularization) for gradient-based feature discovery.
2. Stability Selection: Implements a multi-run aggregation mechanism to ensure consistent and stable feature rankings.
3. Scalability: Demonstrates superior performance over traditional tree-based models (XGBoost) as the dataset grows (up to 10,000 samples).
4. Interpretability: Provides spatial heatmaps of selected pixels, revealing a distinct prioritization of morphological boundaries over central clusters.
  
Project Structure:
The project is organized into three comprehensive Jupyter Notebooks:
01_Data_and_Baselines.ipynb: Data loading, preprocessing, and execution of classical baseline models (XGBoost and 1-NN).
02_Deep_SSFS_Core.ipynb: The core framework — MLP architecture, training loops, Lasso penalty tuning, and the Stability Selection pipeline.
03_Interpretability_and_Results.ipynb: Result analysis, including Jaccard index metrics, accuracy comparisons, and spatial feature visualizations.
