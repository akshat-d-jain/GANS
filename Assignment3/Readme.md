*In this project, we implemented a **Deep Convolutional Generative Adversarial Network (DCGAN)** to generate realistic face images from the **CelebA dataset**. Here’s what we did:*  

### *1. Loaded and Preprocessed CelebA*  
- *Resized and normalized images to **64×64** for stable training.*  
- *Used **PyTorch DataLoader** for efficient batch processing.*    

### *2. Defined DCGAN Architecture*  
- ***Generator (G):*** *Converts random noise into realistic face images.*  
- ***Discriminator (D):*** *Classifies images as real or fake.*  
- *Used **ConvTranspose2d & BatchNorm** in G, **Conv2d & LeakyReLU** in D.*  

### *3. Trained the Model for 10 Epochs*  
- *Used **Binary Cross-Entropy Loss (BCELoss)** to train both G and D.*  
- ***Adam Optimizer** for better convergence.*  
- *Updated D to distinguish real from fake, and G to fool D.*  

### *4. Monitored Training Progress*  
- *Logged losses of G and D over time.*  
- *Generated images after each epoch to visualize improvement.*  

### *5. Visualized Results*  
- *Plotted loss curves to track learning stability.*  
- *Displayed generated face images from random noise.*  

**Final Outcome:** *A trained **DCGAN** that can generate synthetic human face images resembling those in the **CelebA dataset**!*  
