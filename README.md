## Object Detection with Custom Annotated Dataset: Cats and Dogs

### Abstract
This repository presents the implementation of a custom object detection and segmentation model using Mask R-CNN, developed within the Detectron2 framework. The project involved the creation of a bespoke dataset, addressing challenges related to data scarcity and image size mismatches, ultimately resulting in a model capable of accurately detecting and segmenting cats and dogs in images.

### Introduction
Object detection and segmentation are critical tasks in computer vision, with applications spanning various fields. This project explores the use of state-of-the-art models, including RCNN, Fast R-CNN, Faster R-CNN, Mask R-CNN, and YOLO, to address the task of detecting and segmenting cats and dogs. Mask R-CNN was selected for its dual capability of object detection and pixel-level segmentation.

### Methodology
1. **Model Selection**: A comparative analysis of object detection models was conducted, leading to the selection of Mask R-CNN, implemented using the Detectron2 library.

2. **Dataset Creation**:
   - Due to the unavailability of a suitable small-scale dataset, a custom dataset was created. The dataset comprises:
     - **Training Set**: 10 images of dogs and 10 images of cats.
     - **Test Set**: 4 images of dogs and 4 images of cats.
   - Each image was manually annotated using the Labelme tool, resulting in precise object boundary definitions.

3. **Data Preprocessing**:
   - Initial attempts to train the model were hindered by image size mismatches (expected: 224x224 pixels; actual: varied).
   - To resolve this, all images were programmatically resized to 600x800 pixels, necessitating re-annotation of the entire dataset.

4. **Model Implementation**:
   - The environment was configured using Google Colab, with necessary libraries including PyTorch and Detectron2 installed.
   - The resized and re-annotated dataset was uploaded to Google Drive for seamless integration with the Colab environment.

5. **Training and Evaluation**:
   - The model was trained on the custom dataset, with a total runtime of approximately 8 minutes per epoch.
   - Post-training, the model exhibited robust performance in both detecting and segmenting the cat and dog instances within the test images.

### Results
The implemented Mask R-CNN model demonstrated effective object detection and segmentation capabilities, achieving high accuracy despite the limited size of the training dataset. The results underscore the model's potential for application in similar small-scale datasets and further refinement for larger-scale applications.

### Conclusion
This project highlights the feasibility of using custom datasets in conjunction with advanced object detection models to achieve high-performance results. The challenges encountered, including data annotation and preprocessing, provide valuable insights for future endeavors in the field of computer vision.
