## Overview

In this project, a pre-trained YOLOv9c model is utilized with transfer learning to enhance the precision of plastic item detection. By leveraging knowledge from large-scale object detection datasets, transfer learning allows the model to effectively recognize various types of plastic waste. Rather than training the model from scratch, it is fine-tuned on a specialized dataset of plastic waste images, enabling it to adapt its parameters for accurate detection and classification of different plastic items in user-submitted images. 

## Data Preprocessing
a. Merge training datasets which contain same labels of plastic bag, plastic bottle, plastic container, plastic cup, plastic cup, plastic straw and plastic utensil from
- Plastic detection Computer Vision Project (https://universe.roboflow.com/asia-pacific-university-msg4d/plastic-detection-o3dr4)
- Plastic Waste Management Computer Vision Project (https://universe.roboflow.com/yolov5-6agzx/plastic-waste-management-6p8kw)

b. Images in the merged datasets are resized to 640x640 resolution and augmented with multiple strategies to benefit from enhanced model generalization and robustness. These augmentations simulate various real-world scenarios. By diversifying the training data through these augmentations, the model becomes more capable of detecting plastic items in varied orientations, lighting conditions and deformations , leading to improved accuracy and performance across different environmental conditions. The resizing ensures that the model processes images consistently, improving both detection accuracy and computational efficiency during training and inference.

c. Dataset is split into training (80%), validating (10%) and testing (10%) sets with paths listed under data.yml file.
