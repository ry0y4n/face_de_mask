# face_de_mask on Goole Colab

This repository is a fork of the original [face_de_mask](https://github.com/face3d0725/face_de_mask) with changes to make it compatible with running on Google Colab.

## How to Use

1. Upload the necessary files to Google Drive
    1. Download the folder from [this link](https://drive.google.com/drive/folders/1xRN9acdQEb9VDm97ni1mt86UBTsrBlAD?usp=sharing)
    2. Upload the folder to your Google Drive (recommended to put it in `MyDrive/`)

2. Run Colab

    [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ry0y4n/face_de_mask/blob/main/face_de_mask_for_Colab.ipynb)

## My Changes

- Create a fully integrated notebook, including the processing in [Deep3DFaceReconstruction-Pytorch](https://github.com/face3d0725/Deep3DFaceReconstruction-Pytorch) and [3DFace](https://github.com/Juyong/3DFace) repositories necessary to perform face_de_mask
- Fork and modify [face_de_mask](https://github.com/ry0y4n/face_de_mask) to work in the Colab environment
- Fork and modify [Deep3DFaceReconstruction-Pytorch](https://github.com/ry0y4n/Deep3DFaceReconstruction-Pytorch) to work in the Colab environment

*The following is the original README*

---

# face_de_mask

Evaluation code for : [Non-Deterministic Face Mask Removal Based On 3D Priors](https://arxiv.org/pdf/2202.09856.pdf)

## Mask removal ability
![Mask removal ability](results/img2.png)
## Face editing ability
![Face editing ability](results/img1.png)

# Abstract
This paper presents a novel image inpainting framework for face mask removal. Although current methods have demonstrated their impressive ability in recovering damaged face images, they suffer from two main problems: the dependence on manually labeled missing regions and the deterministic result corresponding to each input. The proposed approach tackles these problems by integrating a multi-task 3D face reconstruction module with a face inpainting module. Given a masked face image, the former predicts a 3DMM-based reconstructed face together with a binary occlusion map, providing dense geometrical and textural priors that greatly facilitate the inpainting task of the latter. By gradually controlling the 3D shape parameters, our method generates high-quality dynamic inpainting results with different expressions and mouth movements. Qualitative and quantitative experiments verify the effectiveness of the proposed method.

# Requirements
* Python >= 3.7
* Pytorch >= 1.6
* cv2
* numpy
* PyTorch3D : https://pytorch3d.org/

# Pre-trained Model

https://drive.google.com/drive/folders/1-th-qJQGGgzWQF2qrAGr8njJ9EBWHGIR?usp=sharing

# How to Use

* Create BFM related files following the instructions of this [project](https://github.com/face3d0725/Deep3DFaceReconstruction-Pytorch)
* Download the pre-trained models and put them in the `ckpts` folder. 
* Run test.py

