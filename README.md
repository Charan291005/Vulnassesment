# Assignment 9: Image Classification using CNN (Cats vs Dogs)

## Objective
Develop a Convolutional Neural Network (CNN) to automate classification of pet images into Cats and Dogs, helping an animal welfare organization streamline image sorting.

## Dataset Link
[Cats vs Dogs Dataset - Kaggle](https://www.kaggle.com/datasets/bhavikjikadara/dog-and-cat-classification-dataset)

> Note: Dataset is not included in this repository due to licensing restrictions. Please download it from the Kaggle link above and place it in a `PetImages/` folder with `Cat/` and `Dog/` subfolders before running the notebook.

## Libraries Used
- TensorFlow / Keras
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

## Methodology
1. **Data Understanding**: Explored dataset folder structure, visualized sample images, and identified class counts, image dimensions, and total image count.
2. **Data Preprocessing**: Resized all images to 128x128 pixels, normalized pixel values to 0-1 range, and split data into 80% training and 20% testing using `ImageDataGenerator`.
3. **Model Development**: Built and trained a CNN with three convolutional blocks for 10 epochs using Adam optimizer and binary crossentropy loss.
4. **Model Evaluation**: Assessed performance using accuracy, precision, recall, F1-score, confusion matrix, and accuracy/loss curves.

## CNN Architecture
| Layer | Details |
|---|---|
| Conv2D | 32 filters, 3x3, ReLU |
| MaxPooling2D | 2x2 |
| Conv2D | 64 filters, 3x3, ReLU |
| MaxPooling2D | 2x2 |
| Conv2D | 128 filters, 3x3, ReLU |
| MaxPooling2D | 2x2 |
| Flatten | - |
| Dense | 128 neurons, ReLU |
| Output | 1 neuron, Sigmoid |

**Compilation:** Optimizer = Adam, Loss = Binary Crossentropy, Metric = Accuracy

## Results
- Test Accuracy: *fill in after running*
- Precision: *fill in after running*
- Recall: *fill in after running*
- F1-Score: *fill in after running*
- Confusion Matrix, Accuracy vs Epoch, and Loss vs Epoch plots are generated in the notebook.

## Conclusion
This project demonstrates that CNNs can effectively classify cat and dog images by learning spatial hierarchies of features through convolution and pooling layers. Convolutional layers extract local patterns (edges, textures), while pooling layers reduce dimensionality and control overfitting. Compared to ANNs, CNNs preserve spatial relationships in image data, leading to better accuracy and efficiency for image classification tasks. A limitation of CNNs is their dependency on large labeled datasets and significant computational resources for training.
