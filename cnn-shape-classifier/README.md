# CNN Shape Classifier

A browser-based CNN demo that classifies simple drawings into one of three classes:
- Circle
- Square
- Triangle

The project is built with plain **HTML**, **CSS**, and **JavaScript**.

It includes a drawing canvas, model controls, prediction results, testing, training/fine-tuning, reset, LocalStorage persistence, and an AI/CNN dictionary page.

## Live Demo
https://maorm36.github.io/cnn-shape-classifier/


## Project Overview
This project demonstrates a small Convolutional Neural Network running directly in the browser.

The user draws a shape on the canvas, and the model predicts whether the drawing is a circle, square, or triangle.

The model page includes:

- Canvas drawing editor
- Prediction button
- Training / fine-tuning button
- Synthetic test button
- Reset button
- Model architecture controls
- LocalStorage weight persistence
- Probability bars for the three output classes
- Training and testing log

The project also includes a dictionary page with more than 40 AI and CNN-related terms.

## Main Features

### Shape Drawing
The user can draw a shape directly on the canvas.
Before prediction, the drawing is processed into a standard model input:
1. The visible drawing is detected.
2. The drawing is cropped.
3. The drawing is centered.
4. The drawing is resized to a 28×28 grayscale image.
5. The image is passed into the CNN.

This makes the prediction more stable even when the drawing is small or not perfectly centered.


### Three-Class Classification

The model is limited to three classes:
- Circle
- Square
- Triangle

The output is shown as softmax scores for each class.


### Model Controls

The model page allows controlling:
- Number of convolution layers
- Filters per layer
- Filter size
- Dense neurons
- Learning rate
- Epochs

These controls affect model creation and local fine-tuning.


### Training / Fine-Tuning

The **Train / Fine-Tune** button continues training the current model in the browser.

During training, the model updates its weights and saves the updated model to LocalStorage.


### Testing

The **Test Synthetic Data** button generates sample circle, square, and triangle inputs, then checks the current model's prediction accuracy.


### Reset

The **Reset to Trained Weights** button restores the supplied trained model weights.

This gives the project a stable starting point for testing and demonstration.


### LocalStorage

The current model is saved in browser LocalStorage.

This allows the model to keep its current weights after refreshing the page.


### AI Dictionary

The dictionary page explains important AI and CNN concepts, including:
- CNN
- Convolution
- Filter
- Feature Map
- Pooling
- ReLU
- Softmax
- Forward Pass
- Backpropagation
- Learning Rate
- Epoch
- Loss
- Accuracy
- LocalStorage


## File Structure

cnn-shape-classifier/
├── index.html
├── dictionary.html
├── README.md
├── css/
│   └── styles.css
└── js/
    ├── app.js
    ├── cnn.js
    ├── dictionary.js
    └── pretrained-model.js


## How to Run Locally

No installation is required.

Open the project by double-clicking:

index.html

or open it from a browser.


## How to Use

1. Open the model page.
2. Click **Reset to Trained Weights**.
3. Draw a circle, square, or triangle.
4. Click **Predict Drawing**.
5. View the predicted class and softmax scores.
6. Click **Test Synthetic Data** to test the model.
7. Use **Train / Fine-Tune** to continue local training.
8. Open the **AI Dictionary** page to review the terminology.


## Technologies Used
- HTML
- CSS
- JavaScript
- Canvas API
- LocalStorage
- Custom CNN implementation


## Notes
This is an educational project focused on demonstrating CNN concepts in a simple browser interface.

The model is intentionally limited to three image classes:
- Circle
- Square
- Triangle

Built by Maor Mordo
