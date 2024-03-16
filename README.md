# Potato Disease Classification Project

## Description

I have engineered an end-to-end solution that utilizes cutting-edge machine learning to classify diseases in potato plants. At the heart of this project is a deep learning model trained on a specially curated dataset of potato leaf images. This model is adept at making fine-grained distinctions between early and late blight diseases, two common afflictions of potato crops.

The neural network employed is a convolutional neural network (CNN), renowned for its high performance in image recognition tasks. The model was subjected to a comprehensive training regimen, including rigorous data augmentation and validation, ensuring its robust performance under a variety of conditions such as different lighting and angles of leaf images.

Upon training, I deployed the model onto Google Cloud Platform (GCP) to leverage its scalability and reliability. To interact with the model, I developed a responsive web interface and a cross-platform mobile application suitable for both Android and iOS devices. These platforms are interconnected via a custom API, designed to facilitate easy image uploads of potato leaves by users, followed by the provision of real-time disease classifications.

## Technologies Used

- **Python & TensorFlow:** For model development, thanks to their comprehensive ecosystem and support for deep learning applications.
- **Keras:** To simplify the creation of deep learning models with high-level building blocks.
- **ReactJS:** Chosen for the web application for its component-based architecture, enabling the development of a dynamic and responsive user interface.
- **React Native:** Utilized for the mobile applications due to its ability to compile to native app code, allowing for performance close to native applications.
- **Google Cloud Platform (GCP):** For hosting the model and the server-side components, providing a robust and scalable infrastructure.
- **FastAPI:** For building the API because of its high performance and easy-to-use features for developing and deploying modern web APIs.
- **TensorFlow Lite:** To deploy the deep learning model on mobile devices, enabling efficient model inference on edge devices.
- **Docker & TensorFlow Serving:** For containerizing the model deployment, ensuring consistent environments across development and production settings.

Each technology was chosen to fulfill specific needs in the project: TensorFlow & Keras for their machine learning prowess; ReactJS and React Native for seamless and native-like frontend experiences; GCP for a dependable cloud environment; FastAPI for efficient backend operations; and TensorFlow Lite along with Docker & TensorFlow Serving for optimal model deployment and serving.

## Model Performance Metrics

The performance of the model is exemplary, exhibiting high accuracy in disease classification, as highlighted by the following metrics:

| Metric       | Value                 |
|--------------|-----------------------|
| Loss         | 0.07676056027412415   |
| Accuracy     | 97.44779467582703%    |
| App Accuracy | 99.609375%            |

The above metrics underscore the model's capability to deliver reliable and impactful insights for the management of potato crops.

## Model Architecture

The architecture of the CNN model is sequential, designed for optimal image data processing. The table below provides a summary of the model's layers and their respective functions:

| Layer (type)       | Output Shape           | Param # |
|--------------------|------------------------|---------|
| Conv2D (32 filters)| (None, 254, 254, 32)   | 896     |
| MaxPooling2D       | (None, 127, 127, 32)   | 0       |
| Conv2D (64 filters)| (None, 125, 125, 64)   | 18,496  |
| MaxPooling2D       | (None, 62, 62, 64)     | 0       |
| Conv2D (64 filters)| (None, 60, 60, 64)     | 36,928  |
| MaxPooling2D       | (None, 30, 30, 64)     | 0       |
| Conv2D (64 filters)| (None, 28, 28, 64)     | 36,928  |
| MaxPooling2D       | (None, 14, 14, 64)     | 0       |
| Conv2D (64 filters)| (None, 12, 12, 64)     | 36,928  |
| MaxPooling2D       | (None, 6, 6, 64)       | 0       |
| ...                | ...                    | ...     |
| **Total params**   |                        | 183,747 |
| **Trainable params**|                       | 183,747 |
| **Non-trainable params** |                  | 0       |

The model concludes with dense layers that perform classification based on the features extracted by the convolutional and pooling layers. The
