---
title: "Disease detection in poultry using machine learning"
collection: projects
layout: single
permalink: /projects/desertation
date: 2022-10-17
venue: 'Undergraduate Dissertation'
paperurl: 'https://dissertations.mak.ac.ug/handle/20.500.12281/15939'
---
<!-- This paper is about the number 1. The number 2 is left for future work. -->
Authors: Nalwanga, Patricia
Awath, Javar Abdat
Mwesigwa, Kirabira Mwesigwa
**Namuganga, Emmilly Immaculate**

This project began with building a high-quality image dataset for detecting coccidiosis in chickens. I performed extensive image preprocessing and augmentation, including resizing, normalization, random rotations, flips, zooming, and brightness adjustments to improve model generalization and reduce overfitting. The dataset was split into training, validation, and testing sets to ensure robust performance evaluation.

Using this prepared dataset, I trained an EfficientNet-based convolutional neural network with TensorFlow/Keras to classify chicken images as either Healthy or Coccidiosis. EfficientNet was selected for its strong accuracy–efficiency trade-off, making it ideal for both training and real-time inference. After training, the best-performing model was exported as a .h5 file for production deployment.

For deployment, I developed a full machine-learning inference service that loads and serves the trained model. The backend is built with Starlette + Uvicorn, providing an asynchronous, lightweight, and production-ready environment. At startup, the system automatically downloads the trained model, initializes it for inference, and exposes API endpoints for image upload and analysis.

Users can upload images either through a browser interface or via a JSON REST API. Each uploaded image is automatically preprocessed to the same format used during training—resized, normalized, and converted into a model-ready tensor. The EfficientNet model then predicts whether the chicken is Healthy or affected by Coccidiosis, along with confidence scores. The service returns results as a styled HTML dashboard or structured JSON response for programmatic use.

This project demonstrates end-to-end expertise in dataset preparation, image augmentation, deep learning model training, model optimization, REST API design, asynchronous backend development, and deployment of ML models in a production-style environment.

[Download paper here](https://dissertations.mak.ac.ug/handle/20.500.12281/15939/restricted-resource?bitstreamId=46082)


<!-- Recommended citation: Your Name, You. (2009). "Paper Title Number 1." <i>Journal 1</i>. 1(1). -->
