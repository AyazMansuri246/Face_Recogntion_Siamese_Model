Face Recognition System using Siamese Neural Network

This project implements a Face Recognition (One-Shot Face Verification) system built from scratch using Convolutional Neural Networks (CNNs) and a Siamese Neural Network architecture. The application interface is developed using the Kivy library, and OpenCV is integrated for webcam-based image capture.

Project Overview

1. The system verifies whether two face images belong to the same person using a Siamese Model trained on face pairs.

2. It follows a one-shot learning approach, meaning the model can verify a person’s identity using only one example image.

3. The app captures live images through the webcam and compares them with stored reference images to perform verification in real-time.

Application Setup

1. To run the application, you need the following folder structure inside your project directory:

2. application_data/
   │
   ├── input_image/
   └── verification_images/

3. verification_images/ → contains reference images of the person(s) to be verified.

4. input_image/ → receives the input image captured through the webcam at runtime (via OpenCV in the Kivy app).

Dataset and Training

1. Collected around 350 facial images using a webcam.

2. Applied data augmentation techniques to increase dataset diversity, generating approximately 3,000 images.

3. Created positive pairs (anchor, positive → same person = 1) and negative pairs (anchor, negative → different person = 0) using the LFW (Labeled Faces in the Wild) dataset for negative samples.

4. In total, the model was trained on around 6,000 image pairs.

Model Architecture

Implemented using TensorFlow/Keras.

1. Built a CNN-based embedding model to extract face features.

2. Added a distance layer to compute similarity between embeddings (as used in Siamese Networks).

3. Output: A single value representing whether the two faces are of the same person (1) or not (0).

Next Steps:

1. Improve the model’s performance by expanding the dataset with more diverse facial images (lighting, angles, backgrounds).

2. Fine-tune the network for better feature extraction and robustness under real-world conditions.

3. Plan to upload the model repository soon for community testing and feedback.
