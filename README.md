# AI-Based Handwritten Digit Generation Using DCGAN

## Project Overview

This project focuses on generating realistic handwritten digit images using a Deep Convolutional Generative Adversarial Network (DCGAN).

The model is implemented using TensorFlow and Keras and trained on the MNIST handwritten digit dataset. It consists of two neural networks: a Generator and a Discriminator, which compete against each other to generate realistic handwritten digit images.

## Objectives

- Understand Generative Adversarial Networks (GANs).
- Implement a Generator to create handwritten digit images.
- Implement a Discriminator to distinguish real and generated images.
- Train the DCGAN using the MNIST dataset.
- Generate new handwritten digit samples.
- Visualize Generator and Discriminator training losses.

## Dataset Details

**Dataset:** MNIST Handwritten Digit Dataset

- Total images: 60,000 training images
- Image size: 28 × 28 pixels
- Image type: Grayscale
- Number of classes: 10 (digits 0–9)

The dataset is loaded directly using TensorFlow/Keras.

```python
(x_train, _), (_, _) = tf.keras.datasets.mnist.load_data()
```

## Data Preprocessing

The following preprocessing steps are performed:

1. Reshape images into `(28, 28, 1)`.
2. Convert image values to float32.
3. Normalize pixel values from `[0, 255]` to `[-1, 1]`.
4. Prepare the dataset for GAN training.

## Model Architecture

### 1. Generator

The Generator creates handwritten digit images from random noise.

Main components:

- Dense Layer
- Batch Normalization
- LeakyReLU Activation
- Conv2DTranspose
- Tanh Output Activation

### 2. Discriminator

The Discriminator identifies whether an image is real or generated.

Main components:

- Conv2D
- LeakyReLU Activation
- Dropout
- Flatten
- Dense Layer with Sigmoid Activation

## Training Configuration

| Parameter | Value |
|---|---|
| Dataset | MNIST |
| Framework | TensorFlow / Keras |
| Epochs | 50 |
| Loss Function | Binary Cross-Entropy |
| Optimizer | Adam |
| Learning Rate | 0.0002 |
| Beta 1 | 0.5 |
| Latent Dimension | 100 |

## Results

The DCGAN was trained successfully for 50 epochs.

The project generates handwritten digit-like images using random noise.

### Generated Digit Samples

Generated images are available in the `output_images/` folder.

### Training Loss Graphs

The following graphs are included:

- Generator Loss
- Discriminator Loss
- Combined DCGAN Training Loss

These graphs help visualize the training progress of the Generator and Discriminator.

## Project Structure

```text
GAN_Handwritten_Digit_Generation/
│
├── GAN_Handwritten_Digit_Generation.ipynb
├── generated_images/
├── output_images/
│   ├── generated_digits_grid.png
│   ├── generator_loss.png
│   ├── discriminator_loss.png
│   └── gan_training_loss.png
├── README.md
└── requirements.txt
```

The `generated_images/` folder contains images generated at different training epochs.

## Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Matplotlib
- Jupyter Notebook
- Generative Adversarial Networks (GAN)

## How to Run the Project

1. Clone the repository:

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

2. Navigate to the project folder:

```bash
cd GAN_Handwritten_Digit_Generation
```

3. Install the required libraries:

```bash
pip install -r requirements.txt
```

4. Open the Jupyter Notebook:

```bash
jupyter notebook
```

5. Open `GAN_Handwritten_Digit_Generation.ipynb` and run the cells.

The MNIST dataset will be downloaded automatically when required.

## Conclusion

This project successfully demonstrates handwritten digit generation using a Deep Convolutional Generative Adversarial Network. The Generator learns to create digit-like images, while the Discriminator learns to distinguish real MNIST images from generated images.

The project provides practical experience in deep learning, neural networks, image generation, and Generative AI.

## Author

**Elaiyarasi E**

Data Science with Generative AI

Entri Elevate
