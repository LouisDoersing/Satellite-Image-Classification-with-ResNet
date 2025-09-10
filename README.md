🛰️ Satellite Image Classification with ResNet50

This project applies a ResNet50 convolutional neural network to classify satellite image tiles
into different land use categories. The model was trained on the dataset provided in the
[Kaggle Hackathon Competition](https://www.kaggle.com/competitions/umr-ml-2025-hackathon-2).

📚 Project Objective

The goal of this project was to build a high-accuracy image classification model for land use
and land cover detection using satellite imagery. The challenge was structured as a Kaggle competition
with predefined training and test splits.

⚙️ Technical Details

- Base model: ResNet50 (pretrained on ImageNet)
- Framework: PyTorch + Torchvision
- Optimizer: Adam with learning rate scheduling
- Loss function: CrossEntropyLoss
- Data augmentation: resizing, horizontal/vertical flips, random rotation, color jittering
- Hardware: GPU (Colab T4)

🔍 Dataset

- Training set: 18,000 labeled images
- Validation set: 20% split from the training set
- Test set: 9,000 unlabeled images (competition evaluation)
- Classes: 10 land use categories (e.g., Forest, River, Pasture, Highway, SeaLake, …)

📈 Results

The trained ResNet50 model achieved strong performance:

Metric              | Score
--------------------|-------
Validation Accuracy | 0.9847
Competition Score   | 0.9822

➡️ This demonstrates the effectiveness of transfer learning with ResNet50 on satellite imagery.

🚀 Usage Example

To train the model:

```python
python train.py

