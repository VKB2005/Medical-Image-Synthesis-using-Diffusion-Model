# Medical-Image-Synthesis-using-Diffusion-Model

Generate synthetic **X-ray**, **CT**, **MRI**, and **Ultrasound** images using **pre-built diffusion models** to support medical imaging research.

---

## 📌 Workflow
1. **Dataset Preparation** – Load and preprocess 128×128 grayscale medical images for each modality.  
2. **Model Setup** – Initialize `UNet2DModel` with `DDPMScheduler` for diffusion training.  
3. **Training** – Train modality-specific models (X-ray: 50 epochs, CT: 1000, MRI: 500–5000, Ultrasound: 1000).  
4. **Image Generation** – Generate new images starting from Gaussian noise using the trained model.  
5. **SSIM Evaluation** – Compute Structural Similarity Index to compare real vs generated images.  
6. **Model Saving & Loading** – Save with `model.save_pretrained()` and reload for inference.  
