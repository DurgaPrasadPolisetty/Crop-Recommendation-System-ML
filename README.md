Crop Recommendation System with Explainable AI (XAI)

This project develops an intelligent crop recommendation system that leverages deep learning and Explainable AI (XAI) techniques to provide data-driven insights for optimal agricultural practices. The system processes various datasets related to crop recommendation, fertilizer prediction, crop yield, and environmental parameters to recommend the most suitable crop for given soil and climatic conditions.

## Key Features:

1.  **Data Integration & Preprocessing:** Combines multiple agricultural datasets (`Crop_recommendation.csv`, `Fertilizer Prediction.csv`, `crop_yield.csv`, `mednleydata.csv`) covering soil nutrients (N, P, K), temperature, humidity, pH, rainfall, crop types, and yield information. Missing values are handled, and categorical features are encoded using LabelEncoder, while numerical features are scaled using MinMaxScaler.

2.  **Advanced Deep Learning Model:** Implements a sophisticated deep learning architecture combining Bidirectional LSTM (BiLSTM) layers with Multi-Head Attention. This model is designed to capture complex temporal dependencies and interactions within the input features, leading to accurate crop recommendations.

3.  **Hyperparameter Optimization:** Utilizes `Keras Tuner` with Bayesian Optimization to efficiently search for the best model hyperparameters (e.g., LSTM units, number of attention heads, learning rate) to maximize predictive accuracy.

4.  **Explainable AI (XAI) Integration:** Enhances model transparency and trustworthiness through two primary XAI methods:
    *   **LIME (Local Interpretable Model-agnostic Explanations):** Provides local explanations for individual crop recommendations, highlighting which specific input features (e.g., N, P, K levels, temperature) positively or negatively influenced the model's decision for a particular crop.
    *   **Partial Dependence Plots (PDPs):** Uses a surrogate Random Forest model to generate global explanations, illustrating how the model's prediction for a specific crop changes as a function of one or two input features, while marginalizing over other features. This helps understand the general trend and impact of key parameters.

5.  **Attention Mechanism Visualization:** Visualizes the attention weights from the Multi-Head Attention layer, providing insights into which input features the model focused on when making predictions.

6.  **Latent Space Visualization (PCA):** Employs Principal Component Analysis (PCA) to visualize the model's learned representations (latent features) in a 2D space, helping to understand how different crop classes are clustered and separated by the model.

7.  **Interactive Interface (Gradio):** Provides an intuitive web-based interface using Gradio, allowing users to input soil and climate parameters and receive an instant crop recommendation along with detailed LIME explanations and interactive PDPs.

## Technologies Used:

*   Python
*   Pandas (for data manipulation)
*   NumPy (for numerical operations)
*   TensorFlow/Keras (for deep learning model development)
*   Keras Tuner (for hyperparameter optimization)
*   Scikit-learn (for preprocessing, surrogate models, and evaluation metrics)
*   LIME (for local explainability)
*   Matplotlib & Seaborn (for data visualization)
*   Gradio (for interactive web interface)
