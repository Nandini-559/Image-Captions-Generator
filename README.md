# **Image Captions and Hashtags Generation Using Deep Learning**

This project demonstrates a deep learning approach to automatically generate captions and hashtags for images using a combination of Convolutional Neural Networks (CNN) and Recurrent Neural Networks (RNN). The model is designed for applications such as social media, where captions and hashtags enhance content engagement.

## **Abstract**
Social media posts with captions and hashtags garner more attention. This project automates the generation of captions and hashtags for images using:
- **CNN (VGG19)** for extracting high-level visual features.
- **RNN (LSTM)** for generating captions from extracted features.

The model is trained on the Flickr8k dataset and generates text descriptions and hashtags for input images.

---

## **Features**
- **Caption Generation**: Converts images into coherent textual descriptions.
- **Customizable**: Easily extendable for different datasets and domains.
- **User-Friendly Interface**: UI for uploading images and receiving captions.

---

## **Project Architecture**
### 1. **CNN (VGG19) for Image Features**
- Extracts high-level visual features like textures, edges, and shapes.
- Outputs feature vectors used as input to the RNN.

### 2. **RNN (LSTM) for Caption Generation**
- Combines visual features with word embeddings.
- Generates captions word by word based on context.

---

## **Dataset**
- **Name**: [Flickr8k Dataset](https://www.kaggle.com/datasets/adityajn105/flickr8k)
- **Content**: 8,000 images with five captions each.

---

## **Setup and Usage**
1. Clone this repository:
   ```bash
   git clone https://github.com/Nandini-559/Image-Captions-Generator.git
   cd Image-Captions-Generator
   ```

2. Prepare the dataset:
   - Download the [Flickr8k Dataset](https://www.kaggle.com/datasets/adityajn105/flickr8k) and place it in the `Dataset` folder.

3. Train the model:
   ```bash
   python image_caption_generator.py
   ```

4. Generate captions for new images:
   ```bash
   python captions_generation.py --image <path_to_image>
   ```

---

## **Results**
The model achieved an accuracy of **97.77%**.

### Example 1:
**Input Image and Generated Caption**:  
![Sample Image](https://github.com/Nandini-559/Image-Captions-Generator/blob/master/result.png)

---

## Required Files

This project relies on the following files that are not included in the repository due to size constraints:

1. **`best_model.h5`**: Pretrained model file used for image caption generation.
2. **`features.pkl`**: Pickled features extracted from the dataset using the VGG19 model.
3. **`tokenizer.pkl`**: Tokenizer object pickled after fitting on all captions, used to preprocess text data.
4. **`vgg19_weights_tf_dim_ordering_tf_kernels.h5`**: Weights file for the VGG19 model.

### How to Obtain These Files
You can obtain these files in the following ways:
- **Download**: Use this [Google Drive link](https://drive.google.com/drive/folders/1vugTMRKJSFI7fy1egRvpMyps6fq-mXHx) to download all required files.
- **Generate Locally**:
  - Refer to the `Dataset Preparation` and `Model Training` sections to recreate these files.



