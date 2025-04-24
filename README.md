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

## Explainability with Grad-CAM

To increase farmer trust and validate model decisions, **Grad-CAM** is used. It generates heatmaps indicating which areas of the leaf image were important for prediction. This aids not just in accuracy, but in transparency and real-world adoption.

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
