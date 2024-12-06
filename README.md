<h1 align="center">Bird Image Semantic Segmentation</h1>

<p align="center">
  <a href="https://www.kaggle.com/code/madbonze/bird-image-semantic-segmentation/notebook">Bird Image Semantic Segmentation</a> model trained on the <a href="https://www.kaggle.com/datasets/wenewone/cub2002011">CUB-200-2011</a> dataset using PyTorch
</p>

# Model Architecture

The model is built using the U-Net architecture

![image](https://github.com/user-attachments/assets/d97d5483-83a7-490f-8406-9566f1970a62)

## Training Data

The model is trained on the <a href="https://www.kaggle.com/datasets/wenewone/cub2002011">CUB-200-2011</a> datatset available on Kaggle

## Training Results

**BCE Loss**: Binary Cross Entropy Loss

| Model | Training Loss (BCE) | Validation Loss (BCE) |
| :---: | :-----------: | :-------------: |
| U-Net | 0.0859 | 0.1193 |

## Segmentation Results

**Dataset Domain**: The dataset is of images of birds from North America

### Images from the dataset's domain space

Following are the segmentation masks generated on images from the validation set

![image](https://github.com/user-attachments/assets/f6374e9e-659c-4643-bd79-3df09867d718)
![image](https://github.com/user-attachments/assets/53dc99a9-a68a-4e2c-bccf-07a32f577a55)
![image](https://github.com/user-attachments/assets/0e92d9da-6e1f-4420-8b32-61c516271e60)

### Images from outside the dataset's domain space

Following are the segmentation masks generated on images of birds of India

![image](https://github.com/user-attachments/assets/3b3c81ab-ddd7-48de-b01f-13e375a47d65)
![image](https://github.com/user-attachments/assets/ce93d397-aec2-40cb-943b-db1b07b2b949)
![image](https://github.com/user-attachments/assets/af7e770a-3486-4fed-9b86-84b0f0ac12bb)

## Usage

1. Install dependencies
```bash
pip install torch torchvision matplotlib pillow numpy
```
2. Download the trained model from https://www.kaggle.com/code/madbonze/bird-image-semantic-segmentation/output
3. Download the inference script located at `bird-image-semantic-segmentation-inference.ipynb`
4. Update the model path in the inference script, adjust image links as needed, and execute the cells.

## References

1. Wah, C., Branson, S., Welinder, P., Perona, P., & Belongie, S. (2011). *The Caltech-UCSD Birds-200 Dataset* (Technical Report No. CNS-TR-2011-001). California Institute of Technology.

2. Ronneberger, O., Fischer, P., & Brox, T. (2015). U-Net: Convolutional networks for biomedical image segmentation. In N. Navab, J. Hornegger, W. M. Wells, & A. F. Frangi (Eds.), Medical Image Computing and Computer-Assisted Intervention – MICCAI 2015 (pp. 234–241). Springer. https://doi.org/10.1007/978-3-319-24574-4_28
