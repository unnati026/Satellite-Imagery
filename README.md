# Satellite-Imagery Repository

This repository contains code for a deep learning model to classify satellite imagery into atmospheric and land-related categories. The model is designed to predict atmospheric conditions such as clear, partly cloudy, cloudy, and haze, as well as land-related features like primary rainforest, water bodies, habitation areas, agriculture, roads, cultivation, bare ground, slash-and-burn, selective logging, blooming, blow-down, conventional mines, and artisanal mines.

## Code Structure

- **Data Preprocessing**: The code loads the dataset from a CSV file containing image names and corresponding labels. It then performs one-hot encoding on the labels and splits the data into training and testing sets.

- **Model Architecture**: The deep learning model is implemented using the Keras Sequential API. It consists of convolutional layers, max-pooling layers, batch normalization, and dense layers. The model is compiled with the SGD optimizer and categorical cross-entropy loss, using a custom evaluation metric, F-beta score.

- **Data Augmentation**: Image data generators are employed for both training and testing datasets to augment the images and prepare them for the model. Data augmentation techniques include rescaling, shear, zoom, and horizontal flip.

- **Training**: The model is trained on the atmospheric conditions using the training dataset. The training process includes 10 epochs with a batch size of 16. Validation data is used to monitor the model's performance during training.

- **Testing and Prediction**: The trained model is then used to predict atmospheric conditions for the test dataset. The predictions are stored in a DataFrame along with the corresponding image names.

- **Evaluation**: The accuracy of the model is evaluated using the F-beta score, a metric that considers both precision and recall. The predictions are compared with the true labels, and the overall accuracy is calculated.

## Repository Structure

- **`README.md`**: This documentation file providing an overview of the repository and instructions on running the code.

- **`Satellite_Imagery_Classification.ipynb`**: Jupyter Notebook containing the main code for data preprocessing, model building, training, and evaluation.

- **`planet`**: Folder containing the original dataset from where the train and test sets have been made. It contains the folder **`train-jpg`** which contains all the images in the dataset and the csv file **`train_classes.csv`** containing image names and corresponding labels for training.

- **`train` and `test`**: Folders containing images for training and testing, respectively. These are created during data preprocessing.
