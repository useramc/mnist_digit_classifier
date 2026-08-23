# MNIST Digit Classifier — Neural Network from Scratch using Keras + TensorFlow

A simple, from-scratch image classification mini project that trains a fully-connected (dense) neural network on the **MNIST handwritten digits dataset** using **Keras** with a **TensorFlow** backend.

The model takes a 28x28 grayscale image of a handwritten digit and predicts which digit (0–9) it represents.

---

## Dataset

- **MNIST** — 70,000 grayscale images of handwritten digits (0–9)
  - 60,000 training samples
  - 10,000 test samples
- Each image is 28x28 pixels (784 total pixels when flattened)

---

## Project Workflow

1. **Load Dataset** — Import the MNIST dataset (train/test split) via Keras datasets API.
2. **One-Hot Encoding** — Convert integer labels (0–9) into 10-dimensional one-hot vectors.
3. **Preprocessing**
   - Reshape each 28x28 image into a flat 784-dimensional vector.
   - Normalize pixel values using standardization:
     ```
     normalized_sample = (sample - mean) / (std_dev + epsilon)
     ```
4. **Model Architecture** — Build a densely connected neural network:
   - Input layer (784 units)
   - 2 hidden layers (fully connected / Dense)
   - Output layer (10 units) with **Softmax** activation
5. **Compilation**
   - Optimizer: `SGD` (Stochastic Gradient Descent)
   - Loss function: `categorical_crossentropy`
   - Metric: `accuracy`
6. **Training**
   - Epochs: 3
   - Per-epoch training accuracy: `89.69%` → `94.80%` → `96.03%`
   - Final accuracy: **96.23%**
7. **Evaluation & Visualization**
   - Visualize predictions against actual test images
   - Plot prediction probability distributions per class

---

## Results

| Epoch | Training Accuracy |
|-------|-------------------|
| 1     | 89.69%             |
| 2     | 94.80%             |
| 3     | 96.03%             |

**Final Test Accuracy: 96.23%**

---

## Prerequisites

Make sure you have the following installed before running the project:

- Python 3.8+ (depending on TensorFlow version)
- pip (Python package manager)

### Required Libraries

```bash
pip install tensorflow keras numpy matplotlib
```

| Library      | Purpose                                      |
|--------------|-----------------------------------------------|
| TensorFlow   | Backend engine for Keras                     |
| Keras        | High-level neural network API                |
| NumPy        | Numerical operations & array handling        |
| Matplotlib   | Visualizing predictions and probability plots|

> Tip: It's recommended to use a virtual environment (`venv` or `conda`) to avoid dependency conflicts.

---

## How to Run

1. Clone the repository
   ```bash
   git clone https://github.com/<your-username>/<your-repo-name>.git
   cd <your-repo-name>
   ```

2. (Optional) Create and activate a virtual environment
   ```bash
   python -m venv venv
   source venv/bin/activate      # On Windows: venv\Scripts\activate
   ```

3. Install dependencies
   ```bash
   pip install -r requirements.txt
   ```

4. Run the notebook/script
   ```bash
   jupyter notebook mnist_classifier.ipynb
   # or
   python mnist_classifier.py
   ```

---

## Project Structure

```
├── Notebook_1.ipynb  # Main project file
├── README.md         # Project documentation
├── .gitignore               
                
```

---

## Future Improvements

- Experiment with different optimizers (Adam, RMSprop) for faster convergence
- Add Convolutional Neural Network (CNN) layers to improve accuracy
- Increase number of epochs and add early stopping
- Add a confusion matrix for deeper error analysis
- Deploy the model as a simple web app for live digit recognition

---

## About

This is a **mini project** built to understand the fundamentals of neural networks — from data preprocessing to model training and evaluation — using a classic beginner-friendly dataset (MNIST).

---

