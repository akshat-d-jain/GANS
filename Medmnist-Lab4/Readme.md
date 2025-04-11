Here’s a GitHub-readable **README.md** file for your **GAN Assignment 4**, formatted with sections like project description, installation, usage, and results:

---

### 📝 `README.md`
```markdown
# GAN Assignment 4 - ChestMNIST Image Generation

**Author**: Akshat D Jain  
**PRN**: 22070126136  
**Class**: AIML B3

## 📌 Project Overview

This project implements and compares three types of Generative Adversarial Networks (GANs) using the **ChestMNIST** dataset from `medmnist`:

- ✅ Least Squares GAN (LS-GAN)
- ✅ Wasserstein GAN (WGAN)
- ✅ Wasserstein GAN with Gradient Penalty (WGAN-GP)

Each GAN is trained to generate 28x28 grayscale chest X-ray images.

---

## ⚙️ Installation

Install dependencies using pip:

```bash
pip install torch torchvision tensorboard medmnist
```

---

## 📁 Dataset

We use the `ChestMNIST` dataset from the [`medmnist`](https://github.com/medmnist/medmnist) package. It is downloaded automatically when the script runs.

---

## 🚀 How to Run

You can run the training for each model individually:

```python
# Train LS-GAN
train_lsgan()

# Train WGAN
train_wgan()

# Train WGAN-GP
train_wgan_gp()
```

Each training function:
- Logs metrics to TensorBoard
- Saves sample generated images as `generated_epoch_{n}.png`

---

## 📊 Visualizing Results

Launch TensorBoard to view loss curves and sample images:

```bash
tensorboard --logdir "path/to/log-directory"
```

Set your log directories as follows:
- LS-GAN: `lsgan-epochs`
- WGAN: `wgan-epochs`
- WGAN-GP: `wgan-gp-epochs`

---

## 📷 Output Samples

During training, sample images are saved per epoch:
```
generated_epoch_0.png
generated_epoch_1.png
...
```

These show how the generator improves over time.

---

## 🧠 Architecture Summary

### Generator
- Fully connected layers: [100 → 128 → 256 → 512 → 784]
- Activation: ReLU
- Output: Tanh, reshaped to (1, 28, 28)

### Discriminator
- Fully connected layers: [784 → 512 → 256 → 1]
- Activation: LeakyReLU

---

## 📝 Notes

- LS-GAN uses MSE loss.
- WGAN uses Wasserstein loss with weight clipping.
- WGAN-GP uses gradient penalty for better stability.

---

## 🧼 Cleanup

Don't forget to call:
```python
writer.close()
```
...after training to properly close TensorBoard logging.

---

## 📬 Contact

If you have any queries or suggestions, feel free to reach out to **Akshat D Jain**.

```

Let me know if you'd like a `.zip` with `README.md` + `.py` file together or want help pushing it to GitHub!
