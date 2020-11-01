# Histopathologic-Cancer-Detection

The aim is to create an algorithm to identify metastatic cancer in small image patches taken from larger digital pathology scans. We detect cancer by identifying metastatic tissue in histopathologic scans of lymph nodes using Deep Learning.

### What is Histopathology?

Histopathology is the diagnosis and study of diseases of the tissues, and involves examining tissues and/or cells under a microscope. It is the study of the signs of the disease using the microscopic examination of a biopsy or surgical specimen that is processed and fixed onto glass slides. To visualize different components of the tissue under a microscope, the sections are dyed with one or more stains.

![](https://storage.googleapis.com/kaggle-competitions/kaggle/11848/logos/header.png?t=2018-11-15-01-52-19)

Lymph nodes are small glands that filter the fluid in the lymphatic system and they are the first place a breast cancer is likely to spread. Histological assessment of lymph node metastases is part of determining the stage of breast cancer in TNM classification which is a globally recognized standard for classifying the extent of spread of cancer.
The diagnostic procedure for pathologists is tedious and time-consuming as a large area of tissue has to be examined and small metastases can be easily missed. Hence using Deep Learning and Machine Learning Models provide an efficient alternative.

## Dataset

The dataset is a slightly modified version of the PatchCamelyon benchmark dataset. The original PCam dataset contains duplicate images due to its probabilistic sampling, however, this does not contain duplicates.

It can be downloaded here: https://www.kaggle.com/c/histopathologic-cancer-detection/data

The PatchCamelyon benchmark is a new and challenging image classification dataset. It consists of 327.680 color images (96 x 96px) extracted from histopathologic scans of lymph node sections. Each image is annoted with a binary label indicating presence of metastatic tissue. PCam provides a new benchmark for machine learning models: bigger than CIFAR10, smaller than imagenet, trainable on a single GPU.

PCam packs the clinically-relevant task of metastasis detection into a straight-forward binary image classification task, akin to CIFAR-10 and MNIST. Models can easily be trained on a single GPU in a couple hours, and achieve competitive scores in the Camelyon16 tasks of tumor detection and whole-slide image diagnosis. Furthermore, the balance between task-difficulty and tractability makes it a prime suspect for fundamental machine learning research on topics as active learning, model uncertainty, and explainability.

The data has 2 folders of training and testing images and a file of training labels.

## Model
The proposed model is an ensemble of Xception and MobileNetV2 with Global Average Pooling, 0.5 Dropout, Dense Layer with sigmoid activation, Adam optimization and binary_crossentropy. The model was trained for 10 epoches.

## Result
The model achieved an accuracy of 95%.

## References
- Histopathologic Cancer Detection - Identify metastatic tissue in histopathologic scans of lymph node sections ([Kaggle](https://www.kaggle.com/c/histopathologic-cancer-detection))
- Exploring Data Augmentation with Keras and TensorFlow ([towards data science](https://towardsdatascience.com/exploring-image-data-augmentation-with-keras-and-tensorflow-a8162d89b844))
- Keras Pretrained Models ([Keras](https://keras.io/api/applications/))
- Classification of Histopathological Biopsy Images Using Ensemble of Deep Learning Networks ([Research Paper](https://arxiv.org/pdf/1909.11870.pdf))
