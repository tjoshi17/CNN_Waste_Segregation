# CNN_Waste_Segregation

### Overview

This project implements a Convolutional Neural Network (CNN) to classify waste images into various categories, enabling efficient and automated waste segregation. The goal is to support better waste management by sorting waste into 'Cardboard', 'Food_Waste', 'Glass', 'Metal', 'Other', 'Paper', 'Plastic'.

### Objective

The objective of this project is to implement an effective waste material segregation system using convolutional neural networks (CNNs) that categorises waste into distinct groups. This process enhances recycling efficiency, minimises environmental pollution, and promotes sustainable waste management practices.

The key goals are:
- Accurately classify waste materials into categories like cardboard, glass, paper, and plastic.
- Improve waste segregation efficiency to support recycling and reduce landfill waste.
- Understand the properties of different waste materials to optimise sorting methods for sustainability.

### Data Understanding

The Dataset consists of images of some common waste materials.

1. Food Waste
2. Metal
3. Paper
4. Plastic
5. Other
6. Cardboard
7. Glass

#### Data Description

- The dataset consists of multiple folders, each representing a specific class, such as Cardboard, Food_Waste, and Metal.
- Within each folder, there are images of objects that belong to that category.
- However, these items are not further subcategorised. For instance, the Food_Waste folder may contain images of items like coffee grounds, teabags, and fruit peels, without explicitly stating that they are actually coffee grounds or teabags.

#### Data Processing

- Data Processing steps:
    - Image resizing
    - Normalization
    - One-hot encoding of labels
 
- Data Splitting
    - 80% Training
    - 20% Validation
    - Stratified splitting to maintain class imbalance
 
- Class distribution
  
  <img width="859" height="547" alt="image" src="https://github.com/user-attachments/assets/86ba1b2e-ed81-4f24-b05c-d85457e20855" />

- Verifying correct labels for loaded images
  
  <img width="1568" height="1263" alt="image" src="https://github.com/user-attachments/assets/ab673b6b-6dd1-4704-b520-098e23c03ce3" />

### Model Architecture

- Model consists of 4 convolutional layers with ReLU activation, followed by batch normalization and max-pooling layers.
- Dropout layers were added to prevent overfitting.
- Fully connected layers were used for classification, with final layer using a softmax activation for multi-class classification.

### Training Process

- Model was trained using ADAM Optimizer and Categorical Cross-Entropy Loss.
- Early stopping, model checkpointing were used for optimization and preventing overfitting.

### Performace Metics:
- Accuracy: Model achieved an accuracy of approx. 67% on validation set.
- Precision: Precision scroe is ~67%.
- Recall: Recall Score is ~67%.
- F1 Score: F1 Score is ~67%.
- Confusion Matrix:
  - Confusion matrix revealed that certain class, such as Plastic and Food_Waste, are classified more accurately that others due to class imbalance.

### Conclusion
1. Data-related Improvements

    - Implement data augmentation to address class imbalance.
    - Collect more samples for under represented classes (specially Cardboard).
    - Include more diverse images within each category.

2. Model Enhancements

    - Experiment with deeper architectures or pre-trained models.
    - Implement class weights to handle imbalanced data.
    - Try different optimization strategies and hyperparameters.

3. Practical Applications
   
    - Could be integrated into automated waste sorting systems.
    - Potential for mobile applications for consumer waste sorting.
    - Useful for recycling facilities and waste management education.

### Technologies
- numpy version: 1.26.4
- pandas version: 2.2.2
- seaborn version: 0.13.2
- matplotlib version: 3.10.0
- PIL version: 11.1.0
- tensorflow version: 2.18.0
- keras version: 3.8.0
- sklearn version: 1.6.1

### Author
 > Tejashri Pilla
 >> **Contact** - tejashrii.joshi@gmail.com
