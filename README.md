# Brain Tumor Detection and Segmentation
This project focuses on classification and segmentation of lower-grade gliomas (LGG) from MRI images using advanced deep learning techniques. By leveraging VGG-16 for classification and U-net for segmentation, this system can detect the presence of a tumor and identify its location with high accuracy.
### Features
* Data Augmentation : Techniques like elastic transformations and horizontal flips were used to enhance the small dataset of 3929 images.
* Classification : Utilizes VGG-16, a pre-trained CNN model, for classifying MRI images into tumor or non-tumor categories, achieving an 89% classification accuracy using transfer learning and hyperparameter tuning
* Segmentation : Employs U-net architecture for precise localization of the tumor region in classified images, resulting in a Dice coefficient of 0.81, ensuring accurate tumor segmentation.
### Dependencies
* TensorFlow / Keras
* OpenCV
* Numpy
### Pipeline
1) Data Preprocessing:
* Combined MRI scans with FLAIR segmentation masks to label data.
* Addressed missing sequences by filling gaps with FLAIR scans.
2) Classification Pipeline:
* Base model: VGG-16 pre-trained on ImageNet.
* Added a custom classification head with dropout regularization and a dense output layer using binary cross-entropy loss.
* Optimized using Adam optimizer with early stopping for robust training.
3) Segmentation Pipeline:
* U-net architecture with contracting, bottleneck, and expansive paths.
* Employed Dice loss for training and metrics like Intersection over Union (IoU) for evaluation.
