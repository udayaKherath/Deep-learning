# Detect Deforestation Using Satellite Images (Galenbindunuwewa Region, Sri Lanka)

## Abstract

<div style="text-align: justify;">This project leverages advanced techniques in remote sensing and deep learning to effectively classify areas impacted by deforestation in the Galenbindunuwewa region of Sri Lanka. By employing state-of-the-art models such as the FCN-based U-Net and custom CNN, spatial information is retained during image analysis. Through intensive model training using satellite data from recent deforestation events and meticulous hyperparameter optimization, the accuracy of the algorithms is comprehensively evaluated. The study aims to classify landscapes affected by human-induced deforestation using high-resolution remote sensing and deep learning. Land and forest cover maps were used as base data to construct accurate deep-learning datasets. The overall accuracy of the U-Net model was 95.39%, while the custom CNN achieved an accuracy of 88% in classifying forested and deforested areas.</div>

## Methodology

### Method 1: FCN-based U-Net
- Data Preprocessing
  1.Data Collection and Loading: Satellite images portraying forested and deforested regions were collected, and     
    OpenCV was used to load the images while ensuring data integrity.

### Method 2: Custom CNN

[...]

## Results and Discussion

### Method 1: FCN-based U-Net

The overall accuracy of the U-Net model was 95.39%, with a Jaccard coefficient of 0.8942. The validation set achieved an accuracy of 89.96% and a Jaccard coefficient of 0.8064. These results indicate that the model performed well on unseen test data.

### Method 2: Custom CNN

The custom CNN model achieved an overall accuracy of 88% in classifying forested and deforested areas. The confusion matrix provided valuable insights into the model's strengths and areas for improvement, with a high precision score of 100% but a recall score of 77%.

## Conclusion

This project successfully implemented cutting-edge deep learning techniques, including the FCN-based U-Net and a custom CNN model, for the critical tasks of image segmentation and classification in the context of deforestation detection. The systematic approach, encompassing preprocessing, dataset creation, model training, and evaluation, yielded promising results.

The U-Net model achieved an impressive accuracy of 95.39% in segmenting deforested areas, while the custom CNN model accurately classified forested and deforested areas with an overall accuracy of 88%. The high precision and recall scores demonstrate the models' effectiveness in identifying forested regions and their potential for enhancement.

The findings of this study contribute to more efficient monitoring of damaged forests and the determination of policy priorities for forest area restoration. Further research using improved algorithms and larger datasets is anticipated to result in better estimation of the causes of deforested areas.

## Acknowledgments

[...]

## References

[...]
