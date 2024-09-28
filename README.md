Emotion Recognition:

This is my first machine learning project to display my knowledge about Neural Networks and Convolutional Neural Networks. 
The dataset that was used in this model is the FER2013 dataset from Google. The code was written in Python.
The libraries that were used in this model include: 
  Numpy: to work with Numpy array
  Matplotlib: to plot training and validation accuracy and loss
  Tensorflow: to build a Convolutional Neural Network model.
The hyperparameters used in this model were derived from the study Convolutional Neural Network Hyperparameters optimization for Facial Emotion Recognition by Adrian Vulpe-Grigoraşi; Ovidiu Grigore, cited below:

A. Vulpe-Grigoraşi and O. Grigore, "Convolutional Neural Network Hyperparameters optimization for Facial Emotion Recognition," 2021 12th International Symposium on Advanced Topics in Electrical Engineering (ATEE), Bucharest, Romania, 2021, pp. 1-5, doi: 10.1109/ATEE52255.2021.9425073. keywords: {Training;Electrical engineering;Emotion recognition;Limiting;Databases;Classification algorithms;Convolutional neural networks;hyperparameter optimization;convolutional neural networks;facial emotion recognition;Random Search;FER2013},

  Data preprocessing:
The first thing I did was importing all the neccesary libraries and I also import the datasets and divide it into training and testing datasets. 
Next step is to augmentate the images, since different emotions contain different numbers of images. For example, inside fear folder it contains less images then angry and happy folder. Also, I want the machine to predict in different scenarios, for example, flip the images upside down, mirror the images, normalize the pixels by scaling it between 0 and 1, etc.

  Model architecture: Ensemble CNN
The CNN consists of 4 convolutional layers with filters of size 32 and 64, all using 3x3 kernels.
MaxPooling layers are added after each convolutional layer to reduce the spatial dimensions.
The output from the convolutional layers is flattened and passed through two fully connected dense layers with 1024 and 4096 neurons, respectively, followed by dropout layers (0.2) to prevent overfitting.
The final layer is a softmax layer for classification into 7 different emotion classes (e.g., happy, sad, angry).

The model is compiled using the Adam optimizer and categorical cross-entropy loss function
The model is trained on the augmented training data and use testing dataset to validate, epochs were set at 20.

The test accuracy was at 43% which was not a good performance.
<img width="590" alt="image" src="https://github.com/user-attachments/assets/99ef74fe-bc7e-49af-870c-8e871675ebdf">







