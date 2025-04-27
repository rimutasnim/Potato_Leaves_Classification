# Potato Leaves Classification using CNN and Grad-CAM

## Introduction

Leaf diseases such as **early blight** and **late blight** significantly reduce the productivity of potato crops. These diseases manifest on leaves and can rapidly spread to the entire plant, including the tuber. **Potted potato plants**, grown in household environments or greenhouses, offer an accessible way to cultivate potatoes, but they also require close monitoring of plant health.

Early detection through **image classification** allows for timely intervention. Farmers can use this technology with mobile phones or drones to monitor large fields or small home gardens. This project aims to provide a low-cost, accurate, and explainable solution for potato leaf disease detection.

## Dataset and Classes

The image dataset was divided as follows:
- **Training**: 70%
- **Validation**: 15%
- **Testing**: 15%

The dataset includes three classes:
- Early Blight
- Late Blight
- Healthy Leaf


![sample image](https://github.com/rimutasnim/Potato_Leaves_Classification/blob/main/screenshots/sample_leaves.png?raw=true)

## Deep Learning Models Used

### 1. EfficientNetV2B0
- Uses a compound scaling method and faster training blocks.
- Great balance of speed and accuracy.
- High accuracy and stable predictions in leaf classification.

### 2. DenseNet121
- Dense connections make it easier to learn subtle variations between healthy and diseased leaves.
- Robust for smaller and medium-sized datasets.

### 3. Xception
- Depthwise separable convolution reduces the number of parameters while maintaining accuracy.
- Strong in pattern recognition tasks, helpful in distinguishing between early and late blight.

### 4. InceptionResNetV2
- Combines the benefits of Inception’s feature extraction and ResNet’s efficient training.
- Captures both small and large patterns within leaf structures.

### 5. NASNetMobile
- Lightweight model designed for mobile inference.
- Slightly lower accuracy but useful for low-resource environments.

### Comparison of the TL models

The performance of the following TL models for Potato tuber and leaf disease classi-fication is summed up in Table 02. The result was evaluated using key metrics like F1-Score, Precision, Recall, and Test Accuracy. EfficientNetV2B0 emerged as the best-performing model with an F1-Score, Precision, Recall of 0.98 %, and a Test Ac-curacy of 98.48 %. Similarly, DenseNet121 and Xception performed well with F1-Scores of 0.98 and Test Accuracies of 97.72% and 97.53%. InceptionResNetV2 and NASNetMobile performed lower than those models on the potato tuber dataset. On the other hand, the highest accuracy for the leaf dataset is that model with an F1-Score, Precision, Recall of 0.99 and a Test Accuracy of 99.41 %. Similarly, Dense-Net121 and InceptionResNetV2 performed well with F1-Scores of 0.99 and 0.98 and Test Accuracies of 98.52% and 97.41%. Xception and NASNetMobile performed lower than those models on the potato leaf dataset. On table 01 and 02 we have the performance of each model in tuber and leaf data respectively.               

                                               Comparison of 5 TL models

<div align="center">
  <img src="https://github.com/rimutasnim/Potato_Leaves_Classification/blob/main/screenshots/leaves_5model_comparisn.png?raw=true" alt="model comparison" />
</div>

<div align="center">
  <img src="https://raw.githubusercontent.com/rimutasnim/Potato_Leaves_Classification/c6cffe61fdeb211e44a32b6b42da37170cfbcb99/screenshots/table_leaf.png" alt="model comparison" />
</div>

                                               Best performing models learning Curve

  ![L_curve_for_EfficientNetV2B0_leaves](https://github.com/rimutasnim/Potato_Leaves_Classification/blob/main/screenshots/L_curve_for_EfficientNetV2B0_leaves.png?raw=true)
                                                
                                               Best performing models Confusion Matrix
  <div align="center">
    <img src="https://github.com/rimutasnim/Potato_Leaves_Classification/blob/main/screenshots/C_matrix_leaves.jpg?raw=true" alt="C_matrix_leaves" />
</div>
<div align="center"> Confusion matrix of the EfficientNetV2B0 model for Leaf Dataset </div>


## Explainability with Grad-CAM

To increase farmer trust and validate model decisions, **Grad-CAM** is used. It generates heatmaps indicating which areas of the leaf image were important for prediction. This aids not just in accuracy, but in transparency and real-world adoption.

  <div align="center">
    <img src="https://github.com/rimutasnim/Potato_Leaves_Classification/blob/main/screenshots/gradcam_leaves.png?raw=true" alt="gradcam_leaves" />
</div>

## Benefits to Farmers

- Prevents disease spread through early identification.
- Reduces crop loss and increases yield.
- Low-cost solution deployable on smartphones.
- Can be extended to remote monitoring using drones or IoT sensors.

## Future Enhancements

- Disease severity grading (mild, moderate, severe).
- Real-time deployment with mobile/web apps.
- Incorporation of environmental data like humidity and temperature for disease prediction.
- Multi-language user interface for accessibility in rural areas.
