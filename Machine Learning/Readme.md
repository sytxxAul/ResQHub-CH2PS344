# Motives
### Goals
Machine learning path plays a direct consequential role in the development of the facial recognition model, featured in our application. This facial recognition model is used in the user registration page, matching user's face against the face in their National ID Card. The machine learning path aims to create a facial recognition model that can be integrated into Cloud (via TensorFlow.js) and Mobile (via TensorFlow.Lite).

### Technique
Amidst the uncertainty of how long the development process would take place, we have schemed two scenarios to prevent an unfinished model:
1. Using Siamese Neural Network, trained with 2 images as input and 1 float value as an output (similarity score).
2. Using a regular feature extraction model (CNN), trained with one image as an input and a vector as an output (a vector of facial features locations) and construct these outputs as an input in a Siamese Neural Network, with a float as an output (similarity score).

[[Dataset|Link to Dataset]]

# Dataset
We use Large-scale CelebFaces Attributes (CelebA) Dataset, authored by Ziwei Liu, Ping Luo, Xiaogang Wang, and Xiaoou Tang from The Chinese University of Hong Kong.

### Link
https://mmlab.ie.cuhk.edu.hk/projects/CelebA.html

### Details
This dataset contains:
- 10,177 number of identities,
- 202,599 number of face images, and
- 5 landmark locations, 40 binary attributes annotations per image.

### What Will We Use
1. The aligned and cropped images from the wild images:
   - Original link: https://drive.google.com/file/d/0B7EVK8r0v71pZjFTYXZWM3FlRnM/view?usp=drive_link&resourcekey=0-dYn9z10tMJOBAkviAcfdyQ
   - In our Cloud Storage: https://storage.googleapis.com/count-dracula/CELEBA.zip

2.  The identity labels of the aligned and cropped images:
   - Original link: https://drive.google.com/file/d/1_ee_0u7vcNLOfNLegJRHmolfH5ICW-XS/view?usp=drive_link
   - In our Cloud Storage: https://storage.googleapis.com/count-dracula/labels.txt
   
3. Facial features locations:
   - Original link: https://drive.google.com/file/d/0B7EVK8r0v71pd0FJY3Blby1HUTQ/view?usp=drive_link&resourcekey=0-aFtzLN5nfdhHXpAsgYA8_g
   - In our Cloud Storage: https://storage.googleapis.com/count-dracula/list_landmarks_align_celeba.txt
   
4. Attributes annotations:
   - Original link: https://drive.google.com/file/d/0B7EVK8r0v71pblRyaVFSWGxPY0U/view?usp=drive_link&resourcekey=0-YW2qIuRcWHy_1C2VaRGL3Q
   - In our Cloud Storage: https://storage.googleapis.com/count-dracula/list_attr_celeba.txt