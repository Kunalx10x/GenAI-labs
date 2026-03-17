# CSET419 – Introduction to Generative AI
## Lab 8: Create Artistic Outputs using Neural Art Concepts

## Objective
The objective of this lab is to generate artistic and creative images using Generative Adversarial Networks (GANs) by exploring the latent space of the generator model. Students analyze how different latent vectors influence generated outputs and how different GAN architectures produce diverse visual patterns.

## Dataset
Any suitable image dataset can be used for GAN training. Example datasets include:

- CIFAR-10 Dataset  
- Artwork or Painting Datasets  
- Landscape Image Datasets  
- Object Image Datasets  

Images are preprocessed and normalized before being used for generation.

## GAN Architectures Used

### Basic GAN Model
- Deep Convolutional GAN (DCGAN)

### Advanced GAN Model
- StyleGAN / CycleGAN / BigGAN (any one depending on availability of trained weights)

## Lab Tasks

### 1. Data Preparation
- Load the dataset used during GAN training  
- Normalize image pixel values to the range [-1, 1]  
- Define the latent vector dimension  

### 2. Load Trained GAN Model
- Load the trained Generator network  
- Freeze generator weights  
- Generate images using random latent vectors  

### 3. Latent Space Exploration
- Generate images using multiple random latent vectors  
- Perform interpolation between two latent vectors  
- Observe smooth visual transitions and pattern evolution  

Tasks performed:
- Generated 5–10 artistic samples  
- Implemented linear interpolation in latent space  

### 4. Generate Artistic Outputs
- Use random latent vectors to create artistic images  
- Visualize generated outputs  
- Compare diversity and visual patterns  

## Expected Observations
- GAN generator produces new synthetic images  
- Different latent vectors create artistic variations  
- Interpolation results in smooth transitions between images  
- Generated outputs show creative patterns without copying training images  

## Learning Outcomes
After completing this lab, students will understand:

- How GAN models generate creative visual outputs  
- Importance of latent space in Generative AI  
- Differences between basic and advanced GAN architectures  
- Applications of generative models in AI-based artistic content creation  

## Technologies Used
- Python  
- PyTorch / TensorFlow  
- NumPy  
- Matplotlib  
- Google Colab / Jupyter Notebook  

## How to Run
1. Open the notebook (Lab8_GAI.ipynb)  
2. Run all cells sequentially  
3. Ensure trained generator weights are loaded  
4. Observe generated artistic outputs and interpolation results  

## Repository Structure
Lab8/
│── Lab8_GAI.ipynb  
│── README.md  
│── model_weights/ (optional)  
│── generated_outputs/ (optional)  

## Conclusion
This lab demonstrates how Generative Adversarial Networks can be used to create artistic visual outputs. By exploring latent space representations, students gain practical understanding of how generative models produce diverse images and how interpolation helps visualize learned features.
