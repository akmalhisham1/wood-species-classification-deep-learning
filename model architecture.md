Model Architecture

This document explains the structure and logic behind the two deep learning models used in this project.

1. Xception Model

Xception (Extreme Inception) is a deep CNN architecture that improves both speed and accuracy by replacing traditional convolutions with depthwise separable convolutions.

🔧 Key Ideas

Depthwise convolution → learns spatial patterns

Pointwise convolution → learns channel (feature map) relationships

Fewer parameters, faster training

Excellent for fine-grained image classification (perfect for wood textures)

🏗 Architecture Used in This Project

Input → Xception base (pretrained on ImageNet)

Output feature map: (3 × 3 × 2048)

Flatten layer

Dense layer (4 neurons – Softmax)

Only the Dense layer is trainable (73k parameters)

Total parameters: 20.9 million

🎯 Why It Works Well

Wood textures have fine patterns → Xception excels at capturing subtle details

Highest accuracy: 87%

2. ResNet50 Model

ResNet50 introduces the concept of residual connections, which help extremely deep networks learn effectively by avoiding the “vanishing gradient” problem.

🔧 Key Ideas

Skip connections allow gradients to flow through the network

50-layer deep architecture

Strong baseline for most image-classification tasks

Powerful, but heavier than Xception

🏗 Architecture Used

Input → ResNet50 base (pretrained on ImageNet)

Output: (3 × 3 × 2048)

Flatten layer

Dense layer (4 neurons – Softmax)

Only Dense layer is trainable

Total parameters: 23.6 million

⚠ Observation

Shows slight overfitting

Accurate but less robust

Final accuracy: 82%

3. Comparison Summary
Aspect	Xception	ResNet50
Architecture style	Depthwise separable CNN	Residual CNN
Parameters	20.9M	23.6M
Trainable params	73k	73k
Performance	⭐ Best (87%)	Good (82%)
Overfitting	Low	Medium
Suitable for	Fine-grained textures	General image tasks
4. Why Xception Was Chosen

✔ Captures detailed texture patterns
✔ More efficient
✔ Better generalization
✔ Higher precision, recall, and F1-score across input classes

5. Implementation Notes

Both models use transfer learning, freezing the pretrained layers

Only the classification layer is trained

Works well even with smaller datasets

Maintains fast training time even on CPU/GPU
