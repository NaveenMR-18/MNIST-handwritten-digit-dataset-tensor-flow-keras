# MNIST-handwritten-digit-dataset-tensor-flow-keras# MNIST Handwritten Digit Classification Using TensorFlow/Keras

##  Project Overview
This project implements a simple neural network using TensorFlow/Keras to classify handwritten digits from 0 to 9 using the MNIST handwritten digit dataset.
 project covers the complete machine learning workflow, including dataset exploration, preprocessing, neural network design, training, evaluation, visualization, prediction, and model experimentation.

##  Objectives
The main objectives of this project are:
* Load and explore the MNIST dataset.
* Display sample handwritten digit images.
* Preprocess and normalize image data.
* Build a neural network using TensorFlow/Keras.
* Compile and train the neural network.
* Evaluate the model using test accuracy.
* Visualize training and validation accuracy.
* Visualize training and validation loss.
* Test the model on five handwritten digit images.
* Compare actual and predicted labels.
* Perform an experiment by modifying the neural network using Dropout.
* Compare the performance of the original and experimental models.

---

##  Dataset
The project uses the **MNIST handwritten digit dataset** available through TensorFlow/Keras.
 Dataset Details
| Property          | Description                  |
| ----------------- | ---------------------------- |
| Training images   | 60,000                       |
| Testing images    | 10,000                       |
| Image size        | 28 × 28 pixels               |
| Number of classes | 10                           |
| Classes           | 0, 1, 2, 3, 4, 5, 6, 7, 8, 9 |
| Pixel values      | 0–255                        |
Each image is a grayscale image containing a handwritten digit.

# Technologies Used
* Python
* TensorFlow
* Keras
* NumPy
* Pandas
* Matplotlib
* Jupyter Notebook

##  Neural Network Architecture
The original neural network consists of the following layers:
text
Input Image (28 × 28)
        ↓
Flatten Layer
        ↓
Dense Layer – 128 Neurons
ReLU Activation
        ↓
Dense Layer – 64 Neurons
ReLU Activation
        ↓
Output Layer – 10 Neurons
Softmax Activation
        ↓
Predicted Digit (0–9)
### Model Configuration
| Parameter         | Value                           |
| ----------------- | ------------------------------- |
| Hidden Layer 1    | 128 neurons                     |
| Hidden Layer 2    | 64 neurons                      |
| Hidden Activation | ReLU                            |
| Output Neurons    | 10                              |
| Output Activation | Softmax                         |
| Optimizer         | Adam                            |
| Loss Function     | Sparse Categorical Crossentropy |
| Metric            | Accuracy                        |
| Epochs            | 10                              |
| Batch Size        | 32                              |
| Validation Split  | 20%                             |

# Data Preprocessing
The MNIST images contain pixel values ranging from **0 to 255**.
The pixel values are normalized to a range of **0 to 1** using:
python
x_train = x_train.astype("float32") / 255.0
x_test = x_test.astype("float32") / 255.0
Normalization helps the neural network train more effectively.
# Model Training
The model is trained using the **Adam optimizer** and **Sparse Categorical Crossentropy** loss function.
Example:
python
model.compile(
    optimizer='adam',
    loss='sparse_categorical_crossentropy',
    metrics=['accuracy']
)
The model is trained for **10 epochs** with a batch size of **32**.

# Model Evaluation
After training, the model is evaluated using the MNIST test dataset.
The main evaluation metric is:
* Test Accuracy *
The exact accuracy may vary slightly depending on the training run.
The notebook records the actual test accuracy obtained during execution.
## Visualization
The project includes graphs for:
### Training and Validation Accuracy
The accuracy graph shows how the model's performance changes during training.
### Training and Validation Loss
The loss graph shows how the training and validation loss changes across epochs.
These graphs help analyze the learning behavior of the neural network.
# Digit Prediction
The trained model is tested on **five MNIST test images**.
For each image, the project compares:
text
Actual Label
     vs
Predicted Label
Example:
text
Image 1: Actual = 7, Predicted = 7
Image 2: Actual = 2, Predicted = 2
Image 3: Actual = 1, Predicted = 1
Image 4: Actual = 0, Predicted = 0
Image 5: Actual = 4, Predicted = 4
The actual results are displayed in the Jupyter Notebook.

##  Experiment: Adding Dropout
An additional experiment is performed by adding **Dropout layers** to the neural network.
### Original Model
text
Flatten
   ↓
Dense(128, ReLU)
   ↓
Dense(64, ReLU)
   ↓
Dense(10, Softmax)

# Experimental Model
text
Flatten
   ↓
Dense(128, ReLU)
   ↓
Dropout(0.2)
   ↓
Dense(64, ReLU)
   ↓
Dropout(0.2)
   ↓
Dense(10, Softmax)
Dropout randomly deactivates a fraction of neurons during training and can help reduce overfitting.

# Model Comparison
| Model                    | Test Accuracy |
| ------------------------ | ------------: |
| Original Neural Network  |        XX.XX% |
| Neural Network + Dropout |        XX.XX% |

> Replace `XX.XX%` with the actual results obtained when running the notebook.

# Project Structure
text
MNIST-Neural-Network-Classification/
│
├── MNIST_Neural_Network_Assignment.ipynb
│
├── MNIST_Neural_Network_Report.pdf
│
├── README.md
│
├── requirements.txt
│
└── images/
    ├── sample_digits.png
    ├── accuracy_plot.png
    ├── loss_plot.png
    └── predictions.png
# Installation

 1. Clone the repository
bash
git clone https://github.com/YOUR-USERNAME/MNIST-Neural-Network-Classification.git
 2. Open the project directory
bash
cd MNIST-Neural-Network-Classification
3. Install required libraries
bash
pip install -r requirements.txt
 4. Start Jupyter Notebook
bash
jupyter notebook
 5. Open the notebook
Open:
text
MNIST_Neural_Network_Assignment.ipynb
Run the cells from beginning to end.

# Requirements
The required Python libraries are listed in `requirements.txt`.
text
tensorflow
numpy
pandas
matplotlib
jupyter

#Project Outputs
The project produces the following outputs:
* Sample MNIST digit images
* Neural network model summary
* Training and validation accuracy graph
* Training and validation loss graph
* Test accuracy
* Five digit predictions
* Actual vs predicted labels
* Original vs Dropout model comparison

## Learning Outcomes
After completing this project, the following concepts were understood and implemented:
* MNIST dataset handling
* Image preprocessing
* Data normalization
* Neural network architecture
* Dense layers
* ReLU activation
* Softmax activation
* Model compilation
* Model training
* Validation data
* Model evaluation
* Accuracy and loss visualization
* Digit classification
* Dropout regularization
* Model comparison
* TensorFlow/Keras workflow

## Conclusion
This project demonstrates the use of a simple **Artificial Neural Network** for handwritten digit classification using the MNIST dataset.
The model learns patterns from 28 × 28 grayscale images and classifies them into one of ten digit classes, from **0 to 9**.
The project also demonstrates how training and validation performance can be visualized and how modifying the neural network architecture using Dropout can affect model performance.
##  Author
**Naveen MR**
B.Tech – Computer Science Engineering (AI & ML)
##  References
* TensorFlow Documentation
* Keras Documentation
* MNIST Handwritten Digit Dataset
* Python Documentation
