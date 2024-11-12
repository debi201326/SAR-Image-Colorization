**SAR-Optical Image Translation with CycleGAN**

This repository contains a PyTorch implementation of a CycleGAN model for translating Synthetic Aperture Radar (SAR) images to Optical images and vice versa. The model uses two generators and two discriminators to perform image-to-image translation between SAR and Optical images, with cycle-consistency loss to preserve the content between transformations.

**Dataset and Preprocessing**
The SAR and Optical images are stored in two directories (sar_color/s1 for SAR and sar_color/s2 for Optical). Each image is transformed to a resolution of 256x256 pixels and normalized for model training.

**Model Architecture**
- Generator: The generator network consists of convolutional layers and residual blocks for translating SAR to Optical images and Optical to SAR images.
- Discriminator: The discriminator is a patch-based model to distinguish between real and fake images.

**Training**
- Losses include GAN loss, cycle-consistency loss, and identity loss.
- Optimizers used: Adam with learning rate 0.0002 and betas (0.5, 0.999).
- The training loop iterates through the dataset for a specified number of epochs, updating the generator and discriminator networks iteratively.

**Usage**
- Place the SAR and Optical images in sar_color/s1 and sar_color/s2 folders.
- Run the training loop to train the CycleGAN model.
- After training, the model saves generated images and checkpoints.
- The trained model can then be used to generate Optical images from SAR input using the pre-trained generator.

**Output**
The script saves the generated Optical images in the generated_optical_image.png file, ready for further evaluation or visualization.

