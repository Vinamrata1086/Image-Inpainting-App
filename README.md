# Image Inpainting with SAM and Stable Diffusion

<p align="center">
  <img src="https://github.com/Vinamrata1086/Image-Inpainting-App/blob/main/Project.jpg" width="900">
</p>

## Overview

This project combines the power of the Segment Anything Model (SAM) and Stable Diffusion Inpainting to create a robust image inpainting solution. It accurately identifies masks using SAM and seamlessly fills in missing regions using Stable Diffusion Inpainting.
<p align="center">
  <img src="https://github.com/Vinamrata1086/Image-Inpainting-App/blob/main/inpaint.png" width="500">
</p>


## Tech Stack

- **Gradio:** Used for creating the graphical user interface (GUI) for user interaction.
- **PyTorch:** Deep learning framework for implementing SAM and Stable Diffusion Inpainting.
- **diffusers:** Library for Stable Diffusion Inpainting.
- **PIL (Python Imaging Library):** Used for image processing tasks.
- **scikit-image:** Utilized for calculating Structural Similarity Index (SSIM) and Peak Signal-to-Noise Ratio (PSNR).

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/your-repository.git
   cd your-repository

## Install dependencies:

  ```bash
  pip install -r requirements.txt
```
### Install Segment Anything:

The code requires python>=3.8, as well as pytorch>=1.7 and torchvision>=0.8. Please follow the instructions here to install both PyTorch and TorchVision dependencies. Installing both PyTorch and TorchVision with CUDA support is strongly recommended.

```bash
pip install git+https://github.com/facebookresearch/segment-anything.git
```
or clone the repository locally and install with

```
git clone git@github.com:facebookresearch/segment-anything.git
cd segment-anything; pip install -e .
```
The following optional dependencies are necessary for mask post-processing, saving masks in COCO format, the example notebooks, and exporting the model in ONNX format. jupyter is also required to run the example notebooks.

```
pip install opencv-python pycocotools matplotlib onnxruntime onnx
```


## How to Run

1. Set up the SAM model:
- Download the SAM model checkpoint and place it in the specified directory.

2. Launch the GUI:
  ```
    python your_script.py
  ```
3. Access the GUI:
   - Open a web browser and go to http://localhost:7860 to interact with the inpainting application or running on public URL: https://bf210fbc92b78f5e9a.gradio.live
   - Upload an image, select pixels for masking, provide a prompt, and click "Submit" to see the inpainted result.


## Calculation of SSIM and PSNR
  - SSIM and PSNR values are calculated and printed in the console when the inpainting process is complete.



