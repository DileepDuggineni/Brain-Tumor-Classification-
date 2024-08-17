Brain Tumor Classification 

## **Introduction**

Brain tumors pose a serious threat to public health, requiring timely and accurate diagnosis for e8ective treatment. Conventional brain tumor classification methods, which often rely on manual inspection of medical imaging scans, can be time-consuming and prone to human error. This project aims to address these challenges by leveraging deep learning techniques, particularly Convolutional Neural Networks (CNNs), to develop a model capable of accurately classifying brain tumors from MRI scans.

## **Project Objective**

The primary objective of this project is to create a CNN model that can automatically classify brain tumors from MRI images, potentially aiding healthcare professionals in providing precise diagnoses. I explored different architectures, including a custom CNN, VGG16, ResNet18, and AlexNet, comparing their performance in terms of accuracy.

## **Background**

### **Traditional Machine Learning Approaches**
Early approaches to brain tumor classification utilized traditional machine learning algorithms like SVM, Random Forests, or KNN. These methods relied heavily on manual feature extraction, which required expert knowledge and did not fully capture the complex patterns in MRI images.

### **Deep Learning Approaches**
Recently, CNNs have become the dominant approach for brain tumor classification, as they can automatically learn features from raw MRI images, eliminating the need for manual feature engineering. While some studies have used transfer learning with pretrained models like VGG and ResNet, my approach focuses on training a CNN from scratch, allowing the model to learn task-specific features directly from the data.

## **Dataset and Preprocessing**

### **Dataset**
The dataset used in this project consists of MRI scans of patients with various types of brain tumors, including glioma, meningioma, pituitary adenoma, and no tumor (normal brain scans). The dataset was obtained from [Kaggle](https://www.kaggle.com/datasets/sartajbhuvaji/brain-tumor-classification-mri/data).

### **Preprocessing Steps**
- **Data Splitting:** The dataset was split into training (80%), validation (10%), and test (10%) sets.
- **Label Encoding and One-Hot Encoding:** Tumor classes were encoded and one-hot encoded.
- **Image Loading and Normalization:** Images were resized to 150x150 pixels, converted to RGB, and normalized to the range [0, 1].

## **Model Architecture**

### **Custom CNN**
The custom CNN architecture was built using Keras and consists of multiple convolutional and pooling layers, followed by fully connected layers. This model achieved the highest accuracy among all tested models.

### **Pretrained Models**
I also explored pretrained models like VGG16 and ResNet18, which were fine-tuned for the brain tumor classification task. While these models offered quick training times and leveraged knowledge from large-scale image datasets, they did not outperform the custom CNN.

### **Summary of Model Performance**
| **Model**             | **Test Accuracy**   |
|-----------------------|---------------------|
| Custom CNN            | 94.50%              |
| VGG16                 | 88.38%              |
| ResNet18              | 85.32%              |
| AlexNet               | 87.46%              |
| Pretrained VGG16      | 93.27%              |
| Pretrained ResNet18   | 73.09%              |

## **Results and Findings**

- **Customized CNN:** Achieved the highest accuracy (94.50%), demonstrating the effectiveness of a task-specific architecture.
- **Transfer Learning:** Fine-tuning Pretrained models like VGG16 can significantly enhance performance, with the pretrained VGG16 reaching an impressive accuracy of 93.27%.
- **Challenges with Standard Architectures:** Pretrained ResNet18 showed limitations in this application, highlighting the importance of selecting models that align with specific dataset characteristics.

