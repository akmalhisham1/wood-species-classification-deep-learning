
A transfer-learning approach for classifying wood species using macroscopic images.

1. Overview

This project applies modern deep learning techniques to classify different categories of wood based on image data. Instead of using handcrafted features, the system uses two pretrained CNN architectures — Xception and ResNet50 — and fine-tunes them on a curated wood dataset.

The goal is to build a scalable, automated wood-recognition system suitable for industrial applications, quality inspection, and material selection.

2. Key Features

🔍 Automated wood species classification

🧠 Transfer learning using state-of-the-art CNN models

🧪 Multiple experiments to test hyperparameters

📊 Detailed performance comparison between models

🖼 Image-based input (simple upload → prediction)

⚙ Flexible and extendable code — suitable for future mobile or web deployment

3. Dataset

Source: Zenodo (public dataset)

Total images: 8,544

Type: Macroscopic wood surface images

Preprocessing includes:

Rescaling

Random rotation

Horizontal & vertical flips

Width/height shift

Zoom augmentation

This improves generalization and reduces overfitting during training.

4. Training Summary

The project includes three categories of experiments:

Experiment A — Epoch Count

Tested: 10, 30, 60

Best performance achieved at 60 epochs

Too few → underfit

Too many → risk of overfit

Experiment B — Optimizers

Adam

Stochastic Gradient Descent (SGD)
Result: Adam produced more stable convergence.

Experiment C — Activation Functions

Softmax demonstrated the best accuracy

Alternative activations performed weaker

5. Results
Model	Accuracy	Notes
Xception	87%	Best performance with balanced precision, recall & F1-score
ResNet50	82%	Slight overfitting, lower generalization
6. Why This Project Matters

Wood classification is usually done manually by experts — a slow and error-prone process. By automating the task:

Manufacturers reduce misclassification errors

Product quality improves (e.g., furniture, construction materials)

Faster processing time

Consistent results regardless of human fatigue

7. Future Enhancements

Mobile app integration (camera → prediction)

Larger multi-species dataset

Add Grad-CAM for model explainability

Deploy as API or web service

8. Author

Mohamad Akmal Syahmi
Machine Learning & Data Analyst Enthusiast
