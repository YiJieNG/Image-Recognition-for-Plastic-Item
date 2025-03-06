## Overview

In this project, a pre-trained YOLOv9c model is utilized with transfer learning to enhance the precision of plastic item detection. By leveraging knowledge from large-scale object detection datasets, transfer learning allows the model to effectively recognize various types of plastic waste. Rather than training the model from scratch, it is fine-tuned on a specialized dataset of plastic waste images, enabling it to adapt its parameters for accurate detection and classification of different plastic items in user-submitted images. 

## Data Preprocessing
a. Merge training datasets which contain same labels of plastic bag, plastic bottle, plastic container, plastic cup, plastic cup, plastic straw and plastic utensil from
- Plastic detection Computer Vision Project (https://universe.roboflow.com/asia-pacific-university-msg4d/plastic-detection-o3dr4)
- Plastic Waste Management Computer Vision Project (https://universe.roboflow.com/yolov5-6agzx/plastic-waste-management-6p8kw)

b. Images in the merged datasets are resized to 640x640 resolution and augmented with multiple strategies to benefit from enhanced model generalization and robustness. These augmentations simulate various real-world scenarios. By diversifying the training data through these augmentations, the model becomes more capable of detecting plastic items in varied orientations, lighting conditions and deformations , leading to improved accuracy and performance across different environmental conditions. The resizing ensures that the model processes images consistently, improving both detection accuracy and computational efficiency during training and inference.

c. Dataset is split into training (80%), validating (10%) and testing (10%) sets with paths listed under data.yml file.

## Model Training
The YOLOv9c model is trained using a combination of loss functions, including box loss, classification loss and distribution focal loss (dfl) to optimize the detection of plastic items within images. The training process runs for 100 epochs, during which the model progressively improves its predictions by minimizing these loss metrics.

## Result Analysis
Overall, the blue line representing "all classes" highlights strong performance, achieving a precision score of 1.00 at a confidence threshold of 0.974. This indicates that, across all plastic categories, the model is highly effective at making correct predictions with very few false positives at higher confidence levels.

When analyzing individual classes, the precision for detecting plastic bags remains consistently high, closely following the overall precision curve. This indicates that the model excels in identifying plastic bags with great accuracy.
Plastic bottles also demonstrate strong performance, with reliable detection across different confidence levels.
The curves for plastic containers and cups follow a similar trend, showing a steady increase in precision as confidence rises.
However, precision for detecting plastic straws rises more gradually compared to other categories, suggesting the model may find it more challenging to distinguish straws at lower confidence levels.
Plastic utensils exhibit the most variation in precision, starting lower than other categories but showing improvement at higher confidence thresholds. This indicates that the model requires greater certainty when detecting utensils, but its performance improves as confidence increases.

## Details link
Find out more about the details at: https://www.ngyijie.com/projects/imageRecognition 
