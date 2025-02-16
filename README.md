# activation_visualization_map
Visualizing Activation Maps for Age & Gender Detection
This visualization helps us understand which regions of an image activate specific CNN filters when detecting age and gender.

The number of filters increases progressively from 32 to 512, doubling at each convolutional layer.
As the number of filters increases, the model captures more abstract and complex features:
- Early layers (e.g., 32 filters) detect basic edges and textures.
- Deeper layers (e.g., 512 filters) extract high-level facial features like the jawline, eyes, and lips, which are useful for age and gender classification.
- After extracting these feature-rich representations, we flatten the activation maps into a 1D vector.
- This vector is then passed through fully connected (dense) layers, where the model learns patterns through backpropagation to predict age and gender.

Gender Prediction:

Uses a sigmoid activation function, as it is a binary classification problem (Male/Female).
Age Prediction:

Uses a ReLU activation function, as age is a continuous numerical value (regression problem).
By visualizing these activation maps, we gain insights into how the CNN learns important facial features at different depths of the network.

