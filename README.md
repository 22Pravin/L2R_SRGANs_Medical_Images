# **L2R-SRGANs for Medical Image Super-Resolution**

## **Overview**
This project implements a novel approach to enhance medical image resolution using **L2R-SRGANs** (L2 Regularization Super-Resolution Generative Adversarial Networks). By incorporating L2 regularization into SRGANs, this method achieves improved stability, reduced overfitting, and higher-quality super-resolved images, particularly for medical imaging datasets.

The methodology adapts the SRGAN architecture by:
- Utilizing L2 regularization in the generator and discriminator models to improve generalization.
- Producing high-resolution (HR) images from low-resolution (LR) medical images while preserving anatomical details critical for diagnosis.

---

## **Features**
- **L2 Regularization**:
  - Regularizes the model's weights, preventing overfitting during training.
  - Ensures smooth gradients for stable GAN training.
- **Super-Resolution**:
  - Converts LR medical images into HR images with enhanced clarity.
  - Maintains diagnostic relevance by preserving fine details like edges and textures.
- **GAN-Based Learning**:
  - Employs adversarial training to produce perceptually realistic images.
  - Balances the generator and discriminator for optimal performance.

---

## **Methodology**
1. **Preprocessing**:
   - Input LR images are preprocessed to match the training pipeline.
   - Dataset includes medical imaging modalities (e.g., MRI, CT scans).

2. **Model Architecture**:
   - **Generator**: Incorporates L2 regularization on convolutional layers to improve output stability.
   - **Discriminator**: Uses L2 regularization to maintain a robust adversarial training dynamic.

3. **Loss Functions**:
   - **Content Loss**: Based on the perceptual VGG loss.
   - **Adversarial Loss**: Guides the generator to produce realistic HR images.
   - **L2 Regularization**: Penalizes large weights to encourage generalization.

4. **Evaluation Metrics**:
   - **PSNR (Peak Signal-to-Noise Ratio)**: Quantifies reconstruction quality.
   - **SSIM (Structural Similarity Index Measure)**: Assesses structural fidelity in super-resolved images.

---

## **Installation**
1. Clone this repository:
   ```bash
   git clone <repository-link>
   ```
2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the notebook:
   ```bash
   jupyter notebook L2R-SRGANs_for_Medical_Images.ipynb
   ```

---

## **Usage**
1. Load your medical image dataset in LR format.
2. Configure the training parameters in the notebook (e.g., learning rate, batch size).
3. Train the L2R-SRGAN model.
4. Visualize and evaluate the generated HR images.

---

## **Results**
- L2R-SRGANs demonstrate superior performance compared to traditional SRGANs, with reduced overfitting and enhanced medical image quality.
- Example metrics:
  - **PSNR**: Achieved an average improvement of 5% over baseline SRGAN.
  - **SSIM**: Demonstrated better structural preservation in HR outputs.

---

## **References**
- SRGAN architecture and improvements derived from: *Photo-Realistic Single Image Super-Resolution Using a Generative Adversarial Network* by Ledig et al.
- Adapted L2 regularization techniques for enhanced training stability.

---
