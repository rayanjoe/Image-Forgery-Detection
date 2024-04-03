# Image-Forgery-Detection
To detect spliced forged images 
The PDF outlines a comprehensive methodology for detecting image forgery, specifically focusing on splicing-based manipulations using advanced digital signal processing and machine learning techniques. The core technology stack includes the Discrete Wavelet Transform (DWT), Edge Weighted Local Binary Patterns (DRLBP), and Support Vector Machine (SVM) classifier. This detailed explanation aims to be suitable for a technical audience, such as that found on GitHub.

### Project Overview

**Title**: Image Splicing-Based Forgery Detection Using Discrete Wavelet Transform and Edge-Weighted Local Binary Patterns

**Authors**: Rayan Joseph Bastine Irudayaraju, Lavanya Jandyam, Mahalaxmi Anumula

**Abstract**: The document discusses the prevalent issue of digital image forgery, highlighting the challenges in detecting alterations made through sophisticated image editing tools. It underscores the importance of image authentication in various fields such as web media, surveillance, and legal evidence. The focus is on addressing forgery through splicing, where parts of different images are combined, and the manipulation is often concealed through post-processing techniques like blurring and noise addition.

### Introduction

The goal of the project is to develop a model that autonomously determines whether an image has been tampered with, particularly through splicing. The methodology leverages the DWT for decomposing images into sub-bands to identify inconsistencies and employs the DRLBP for coding these coefficients. The SVM classifier is then used for the final determination of forgery.

### Dataset

- **Columbia-Image-Spliced-Dataset**: Utilized for its diverse range of images, encompassing over 12000 images each with five captions, allowing for extensive training and validation.
- **Columbia-Image-Spliced-Dataset**: Utilized for its diverse range of images, encompassing less than 1000 images each with five captions, allowing for extensive training and validation.

### Methods

1. **DWT-DRLBP Descriptor**: Combines DWT's ability to decompose images into frequency sub-bands with DRLBP's texture description capabilities. This hybrid descriptor is sensitive to the subtle inconsistencies introduced by splicing.
   
2. **Wavelet Decomposition**: Applies DWT on chroma components, separating the image into high and low-frequency bands to capture contrast variations indicative of manipulation.

3. **DRLBP Histograms**: Quantifies discriminative image patterns, like edges and corners, using histograms of local binary patterns, enhancing detection sensitivity to alterations.

4. **Computation of DWT-DRLBP Descriptor**: Aggregates local DRLBP patterns from the image's sub-bands, creating a comprehensive descriptor that captures structural changes indicative of forgery.

### Model Training

- A **Support Vector Machine (SVM)** classifier is trained to differentiate between authentic and spliced images, with a kernel trick employed to manage the non-linear characteristics of image forgery datasets.

### Model Performance

- **Validation Accuracy**: Achieved approximately 72.60% on both the Columbia and CASIA v2.0 datasets in 500 fits, indicating the model's capability but also suggesting potential overfitting issues.

### Results

- **Test Outcomes**: Varied performance across datasets, with the model successfully identifying tampered images in some cases but failing in others, particularly when the gradient differences between original and spliced areas were minimal.

### Conclusion

The project presents a novel approach to detecting splicing-based image forgeries, achieving a significant accuracy level. It demonstrates the effectiveness of combining DWT and DRLBP for capturing and quantifying image inconsistencies. However, challenges remain, particularly in distinguishing highly sophisticated forgeries, suggesting areas for future research and improvement, such as exploring more complex models or incorporating additional data augmentation techniques.

### Technical Contributions for GitHub

This project contributes significantly to the field of digital image forensics by:

1. Introducing a novel descriptor combining DWT and DRLBP for enhanced detection of image splicing.
2. Demonstrating the application of machine learning, specifically SVM, in classifying images as tampered or authentic based on textural and structural inconsistencies.
3. Offering a comprehensive evaluation using real-world datasets, providing a benchmark for future research in image forgery detection.

The methodologies, datasets, and findings detailed in this document offer a solid foundation for further exploration and development in the area of digital image authentication and forensics.
