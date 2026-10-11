
# StyleGAN-Inspired Image Generation with TensorFlow

A learning-oriented implementation of a StyleGAN-inspired Generative Adversarial Network (GAN) using TensorFlow/Keras and the CIFAR-10 dataset.

> Note: This is an educational implementation inspired by StyleGAN concepts, not an official reproduction of NVIDIA's StyleGAN architecture.

## 🚀 Features

- TensorFlow and Keras implementation
- CIFAR-10 dataset preprocessing
- Style mapping network
- Learned constant input
- Styled convolution layers
- Adaptive Instance Normalization (AdaIN)-inspired style modulation
- Noise injection
- Generator and discriminator training
- Training loss visualization
- Generated image grids
- Style mixing
- Latent-space interpolation

## 🧠 How It Works

### Generator
The generator creates synthetic images from random latent vectors.

1. Generates a latent vector `z`.
2. Maps it into a style vector `w`.
3. Starts synthesis from a learned constant tensor.
4. Applies styled convolution layers and noise injection.
5. Produces a 32×32 RGB image.

### Discriminator
The discriminator uses convolutional layers to distinguish real CIFAR-10 images from generated images.

## 📊 Dataset

- **Dataset:** CIFAR-10
- **Training samples:** 20,000
- **Image dimensions:** 32 × 32 pixels
- **Channels:** RGB
- **Normalization:** Approximately [-1, 1]

## ⚙️ Training Configuration

| Parameter | Value |
|---|---|
| Framework | TensorFlow / Keras |
| Latent dimension | 128 |
| Style dimension | 128 |
| Batch size | 64 |
| Epochs | 10 |
| Optimizer | Adam |
| Learning rate | 0.0002 |
| Random seed | 42 |

## 📈 Recorded Results

The notebook reports the following model sizes:

- Generator parameters: 1,044,651
- Discriminator parameters: 428,385
- Final discriminator loss: approximately 1.386
- Final generator loss: approximately 0.693

These loss values alone do not establish image quality. Review the generated samples to evaluate the results.

## 🛠️ Requirements

- Python 3.10+
- TensorFlow
- NumPy
- Matplotlib
- Jupyter Notebook or Google Colab

Install the dependencies:

```bash
pip install tensorflow numpy matplotlib jupyter
```

## ▶️ How to Run

1. Clone or download this repository.
2. Open the notebook in Jupyter Notebook or Google Colab.
3. Run the cells in order.
4. Allow CIFAR-10 to download.
5. View the generated images, loss curves, style mixing, and latent interpolation results.

## 📁 Project Structure

```text
stylegan-inspired/
├── README.md
└── stylegan_cifar10.ipynb
```

Rename your uploaded notebook to `stylegan_cifar10.ipynb`, or change the filename above to match yours.

## ⚠️ Limitations

- Generates small 32×32 images.
- Uses a subset of CIFAR-10.
- Training is intended for educational experimentation.
- Does not implement every component of the official StyleGAN architecture.
- Generated image quality requires visual evaluation.

## 🔮 Future Improvements

- Train for more epochs.
- Save model checkpoints.
- Experiment with larger datasets and image resolutions.
- Evaluate image quality using metrics such as FID.
- Compare results with the official StyleGAN2-ADA implementation.

## 📚 References

- [TensorFlow](https://www.tensorflow.org/)
- [CIFAR-10 Dataset](https://www.cs.toronto.edu/~kriz/cifar.html)
- [Official NVIDIA StyleGAN2-ADA Repository](https://github.com/NVlabs/stylegan2-ada-pytorch)

## 📄 License

Choose a license before publishing this repository. Review the license requirements of any third-party code you use.
