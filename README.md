# Detect Deforestation Using Satellite Images (Galenbindunuwewa Region, Sri Lanka) 

## Abstract

<div style="text-align: justify;">This project leverages advanced techniques in remote sensing and deep learning to effectively classify areas impacted by deforestation in the Galenbindunuwewa region of Sri Lanka. By employing state-of-the-art models such as the FCN-based U-Net and custom CNN, spatial information is retained during image analysis. Through intensive model training using satellite data from recent deforestation events and meticulous hyperparameter optimization, the accuracy of the algorithms is comprehensively evaluated. The study aims to classify landscapes affected by human-induced deforestation using high-resolution remote sensing and deep learning. Land and forest cover maps were used as base data to construct accurate deep-learning datasets. The overall accuracy of the U-Net model was 95.39%, while the custom CNN achieved an accuracy of 88% in classifying forested and deforested areas.</div>

## Methodology

### Method 1: FCN-based U-Net

![Figure 1](https://raw.githubusercontent.com/udayaKherath/Final-Year-Research/main/img3.png)
- Data Preprocessing
  - Data Collection and Loading: Satellite images portraying forested and deforested regions were collected, and OpenCV was used to load the images while ensuring data integrity.
  - Image Cropping and Resizing: Images were cropped and resized to consistent dimensions using the Python Imaging Library (PIL) to preserve aspect ratios.
  - Patch Extraction and Normalization: Cropped images were converted into NumPy arrays, and the patchify function was used to divide them into smaller patches. Min-max scaling was applied to normalize pixel values of individual patches.
  - Mask Loading and RGB Conversion: Corresponding mask images indicating deforested regions were loaded and converted to the RGB color space using OpenCV.
  - Mask Cropping and Patching: Mask images were cropped, resized, and divided into patches aligned with the corresponding image patches.

- Dataset Creation and Preprocessing
  - Pairing Image and Mask Patches: Image and mask patches were associated to create a compatible dataset for training.
  - Label Encoding and Categorization: Mask patches were converted into categorical labels representing deforested and non-deforested areas.
 
- Deep Learning Model Architecture
  - The FCN-based U-Net architecture was employed, consisting of an encoder and decoder process. The encoder process involved image compression and feature extraction using the rectified linear unit (ReLU) during activation. The decoder process restored the image while preserving spatial information using the same pooling layer as the encoder.
 
- Model Training and Evaluation
  - Dataset Splitting: The paired dataset was divided into training and testing subsets.
Loss Function and Optimization: Dice Loss and Categorical Focal Loss functions were defined to guide the optimization process and ensure accurate segmentation of deforested areas.

  - Model Training: The model was compiled and trained over multiple epochs using the segmented image data from the training set.
  - Performance Evaluation: The model's performance was monitored using metrics such as accuracy and the Jaccard coefficient (IoU). The validation set was used to assess the model's accuracy on unseen data.
  - Analysis and Visualization: Visual representations of training and validation loss trends, as well as IoU trends, were plotted to assess model convergence and identify potential overfitting.

- Model Visualization
  - U-Net Performance: The U-Net model's performance was visualized by generating sample predictions, displaying original images, true masks, and predicted masks to assess segmentation accuracy visually.
  - CNN Confusion Matrix: A confusion matrix was generated and displayed to evaluate the CNN model's classification performance, providing insights into its ability to correctly classify forest and deforestation images.

## Results and Discussion
The overall accuracy of the U-Net model was 95.39%, with a Jaccard coefficient of 0.8942. The validation set achieved an accuracy of 89.96% and a Jaccard coefficient of 0.8064. These results indicate that the model performed well on unseen test data.

## Conclusion

This project successfully implemented cutting-edge deep learning techniques, including the FCN-based U-Net and a custom CNN model, for the critical tasks of image segmentation and classification in the context of deforestation detection. The systematic approach, encompassing preprocessing, dataset creation, model training, and evaluation, yielded promising results.

The U-Net model achieved an impressive accuracy of 95.39% in segmenting deforested areas, while the custom CNN model accurately classified forested and deforested areas with an overall accuracy of 88%. The high precision and recall scores demonstrate the models' effectiveness in identifying forested regions and their potential for enhancement.

The findings of this study contribute to more efficient monitoring of damaged forests and the determination of policy priorities for forest area restoration. Further research using improved algorithms and larger datasets is anticipated to result in better estimation of the causes of deforested areas.
