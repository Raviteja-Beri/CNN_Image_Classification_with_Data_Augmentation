# 🧠 CNN_Image_Classification_with_Data_Augmentation

This project demonstrates the use of a **Convolutional Neural Network (CNN)** for image classification, enhanced with various **data augmentation** techniques to improve model generalization and reduce overfitting. It leverages **TensorFlow** and **Keras** to build, train, and evaluate the deep learning model.

---

## 📌 Objective

To build a robust CNN-based image classifier capable of learning from limited training data using real-time data augmentation strategies.

---

## 🗂️ Dataset

- The dataset is organized into `training_set` and `test_set` directories.
- Images are structured in subfolders corresponding to their respective classes (binary classification problem).
- Loaded using `ImageDataGenerator` from `keras.preprocessing.image`.

---

## 🧪 Data Augmentation Techniques

Implemented using **`ImageDataGenerator`** with the following transformations:
- `rescale=1./255` – Normalization of pixel values
- `shear_range=0.2` – Shearing of images
- `zoom_range=0.2` – Random zooming
- `horizontal_flip=True` – Random horizontal flips
- `rotation_range=30` – Image rotation
- `width_shift_range=0.2` – Horizontal shifts
- `height_shift_range=0.2` – Vertical shifts

> These techniques help the model generalize better by simulating a wider variety of image conditions.

---

## 🧠 Model Architecture

A **Sequential CNN** model was built using `tensorflow.keras.models.Sequential` with the following layers:

| Layer Type              | Details                                               |
|-------------------------|--------------------------------------------------------|
| `Conv2D`                | Filters: 32, Kernel Size: (3,3), Activation: **ReLU**  |
| `MaxPooling2D`          | Pool Size: (2,2)                                       |
| `Conv2D`                | Filters: 32, Kernel Size: (3,3), Activation: **ReLU**  |
| `MaxPooling2D`          | Pool Size: (2,2)                                       |
| `Flatten`               | Flattens 2D to 1D                                      |
| `Dense`                 | Units: 128, Activation: **ReLU**                       |
| `Dense` (Output Layer)  | Units: 1, Activation: **Sigmoid**                      |

---

## ⚙️ Compilation and Training

- **Loss Function**: `binary_crossentropy`
- **Optimizer**: `adam`
- **Metrics**: `accuracy`
- **Epochs**: 25
- **Batch Size**: 32

* Python:
```
model.compile(optimizer='adam', loss='binary_crossentropy', metrics=['accuracy'])
```

* Model is trained using:
```
model.fit(training_set, epochs=25, validation_data=test_set)
```

## Technologies & Modules Used
1. Python
2.TensorFlow 2.x
3. Keras
4. Numpy
5. Matplotlib (for visualization)
6. Keras ImageDataGenerator
7. Git Large File Storage (Git LFS)

---
## Thank You
---
