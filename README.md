**Cross-Domain SAR to RGB Image Translation using Conditional GAN with Perceptual Guidance **

Synthetic Aperture Radar (SAR) images are a valuable source of remote sensing data due to their ability to capture high-resolution surface information regardless of weather and lighting conditions. However, SAR images are typically grayscale and lack the semantic richness of optical images, making them difficult for human interpretation.

This project proposes a deep learning-based SAR image colorization method using a Conditional Generative Adversarial Network (cGAN).

🔧 Key Features
U-Net-based Generator: Transforms single-channel SAR images into colorized RGB images, preserving spatial details.
Discriminator: Encourages local realism and texture consistency in generated outputs.
Composite Loss Function:
Perceptual Loss (from pre-trained VGG19)
Pixel-wise L1 Loss
Adversarial Loss

📚 Dataset
We train our model on paired SAR-optical image datasets covering a variety of land cover classes, enabling better generalization and semantic mapping.

🎯 Results
The colorized outputs:
Retain fine spatial patterns
Show high visual realism
