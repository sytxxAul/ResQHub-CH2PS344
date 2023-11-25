### Ground Truth
Machine learning path plays a direct consequential role in the development of the facial recognition model, featured in our application. The machine learning path aims to create a facial recognition model that can be integrated into Cloud (via TensorFlow.js) and Mobile (via TensorFlow.Lite).

### Technique
Amidst the uncertainty of how long the development process would take place, we have schemed two scenarios to prevent an unfinished model:
1. Using Siamese Neural Network, trained with 2 images as input and 1 float value as an output (similarity score).
2. Using a regular feature extraction model (CNN), trained with one image as an input and a vector as an output (a vector of facial features locations) and construct these outputs as an input in a Siamese Neural Network, with a float as an output (similarity score).

[[Dataset|Link to Dataset]]