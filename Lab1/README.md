# GenAI-Lab-1-Cat-Classification
# GenAI Lab 1: Synthetic Dataset Generation & Transfer Learning Analysis

## 📌 Project Overview
This project investigates the effectiveness of **Generative AI** for creating synthetic datasets and evaluates the impact of **Transfer Learning** on model performance under data scarcity constraints.

**Key Objectives:**
1.  **Synthetic Data Generation:** Created a dataset of 40+ distinct cat species (wild & domestic) using **Stable Diffusion v1.5**.
2.  **Baseline Training:** Built and trained a Custom CNN from scratch.
3.  **Transfer Learning:** Fine-tuned a pre-trained **ResNet50** model.
4.  **Few-Shot Learning:** Implemented a prototypical baseline using frozen ResNet features.

## 📊 Results Summary
We compared three different approaches on the synthetic dataset (~600 images).

| Model Architecture | Accuracy | Key Observation |
|-------------------|:--------:|-----------------|
| **Custom CNN** | **20.73%** | Struggled significantly due to "Data Scarcity" (only ~15 images/class). |
| **Few-Shot (Frozen)** | **~80.50%** | Demonstrated that pre-trained feature extractors are robust even without fine-tuning. |
| **ResNet50 (Fine-Tuned)** | **80.49%** | **Best Performance.** Adapting pre-learned weights to the specific domain yielded a ~4x improvement over the custom model. |

## 🧪 Methodology

### 1. Dataset Creation
* **Tool:** Stable Diffusion (`runwayml/stable-diffusion-v1-5`)
* **Prompt Engineering:** Used high-fidelity prompts (e.g., *"National Geographic photography of a [Species], 8k, cinematic lighting"*) to ensure distinct visual features.
* **Volume:** Generated ~15 images per class for 40 classes.

### 2. Model Architectures
* **Custom CNN:** A 4-layer Convolutional Neural Network with Batch Normalization, MaxPooling, and Dropout. Trained with Data Augmentation (Rotation, Flips, Color Jitter).
* **ResNet50:** A standard ResNet50 backbone pre-trained on ImageNet.
    * *Frozen Baseline:* Used as a fixed feature extractor with a K-Nearest Neighbor classifier.
    * *Fine-Tuned:* Unfroze the final fully connected layer to adapt to the 40 cat species.

## 🚀 How to Run

### Prerequisites
* Python 3.8+
* GPU recommended (Google Colab T4 or better)

### Installation
1.  Clone the repository:
    ```bash
    git clone [https://github.com/YOUR_USERNAME/GenAI-Lab-1-Cat-Classification.git](https://github.com/Kunalx10x/GenAI-Lab-1-Cat-Classification.git)
    cd GenAI-Lab-1-Cat-Classification
    ```
2.  Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```

### Usage
1.  Open `GAI_1_2.ipynb` in Jupyter Notebook or Google Colab.
2.  Run the **Dataset Generation** cells to create the images (or upload your own zip).
3.  Run the **Training** cells to reproduce the Custom CNN and ResNet50 results.
4.  Run the **Evaluation** cells to see the confusion matrices and final comparison graph.

