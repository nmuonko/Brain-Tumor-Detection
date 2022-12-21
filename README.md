# Brain-Tumor-Detection

Brain-Tumor-Detector
Building a detection model using a convolutional neural network in Tensorflow & Keras.
Used a brain MRI images data founded on Kaggle.

About the data:

The dataset contains 2 folders: yes and no which contains 253 Brain MRI Images. The folder yes contains 155 Brain MRI Images that are tumorous and the folder no contains 98 Brain MRI Images that are non-tumorous.

Getting Started
Note: sometimes viewing IPython notebooks using GitHub viewer doesn't work as expected, so you can always view them using nbviewer.

Data Augmentation:
Why did I use data augmentation?

Since this is a small dataset, There wasn't enough examples to train the neural network. Also, data augmentation was useful in taclking the data imbalance issue in the data.

Further explanations are found in the Data Augmentation notebook.

Before data augmentation, the dataset consisted of:
155 positive and 98 negative examples, resulting in 253 example images.

After data augmentation, now the dataset consists of:
1085 positive and 980 examples, resulting in 2065 example images.

Note: these 2065 examples contains also the 253 original images. They are found in folder named 'augmented data'.

Data Preprocessing
For every image, the following preprocessing steps were applied:

Crop the part of the image that contains only the brain (which is the most important part of the image).
Resize the image to have a shape of (240, 240, 3)=(image_width, image_height, number of channels): because images in the dataset come in different sizes. So, all images should have the same shape to feed it as an input to the neural network.
Apply normalization: to scale pixel values to the range 0-1.
Data Split:
The data was split in the following way:

70% of the data for training.
15% of the data for validation.
15% of the data for testing.
Neural Network Architecture
This is the architecture that I've built:
