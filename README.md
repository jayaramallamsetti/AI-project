# Classification of Bacteria Species images using Machine Learning Techniques

# Objective:

To implement both supervised and unsupervised learning methodologies for bacterial identification and classification.

# Introduction:

1) The use of deep learning in bacteria colony classification can potentially enhance the speed and efficiency of the analysis process.
2) Deep learning algorithms, once trained, can rapidly process large volumes of images and provide automated and consistent classification results, reducing the burden on 
   microbiologists and enabling faster decision-making at places having lack of  facilities.
3) Many methods have been proposed for improving transfer learning for bacterial colony classification using deep learning. Researchers have trained convolutional neural   
   networks (CNNs) on a dataset of bacterial colony images and achieved high accuracy in classifying E. coli and K. pneumoniae colonies.
# Dataset Collection
1) Images captured at 5 cm and 10 cm distances for diversity.
2) Consistent lighting in well-lit rooms (no natural sunlight).

![image](https://github.com/user-attachments/assets/56854742-26df-4e5c-bbb2-076b8dce5017)
![image](https://github.com/user-attachments/assets/bc1bc37a-441d-4a8e-8e19-56909175aac2)

# Pre-processing

**Unsupervised Learning**

Original images: 768x1024x3 dimensions, Resized to 256x256x3 for Unsupervised Learning.

**Supervised Learning Preprocessing - AlexNet**:

Data Augmentation for diversity:
   Rotation (up to 20 degrees)
   
   Width and height shifts (up to 20%)
   
   Shearing transformations
   
   Zooming in/out (20% range)
   
   Horizontal flipping
   
   Pixel value normalization to [0, 1]


# Method Selection and Justification:

**Unsupervised K-Means Clustering for Multiclass Classification:**
 
**K-Means Clustering:**

Selected for the following reasons:

Simplicity: User-friendly with an intuitive logic.

Non-Parametric: Freedom from strict data distribution assumptions.

Complex Pattern Detection: Proficient in capturing intricate patterns, essential for nuanced bacterial species differences.

Scalability: Efficient handling of extensive datasets, vital for real-world applications.

**Supervised learning based architectures:**


  a)**AlexNet**:
  
   It is well-suited for image classification tasks and excels at capturing intricate details in images. This is crucial for the complex task of bacterial colony
   classification.
   
 b) **Vision Transformation**(ViT):
 
    1) It was selected to explore the use of transformer-based models in image classification.
    2) ViT represents a departure from traditional convolutional networks by using self-attention mechanisms. It is known for its effectiveness in computer vision tasks and          may excel at capturing long-range dependencies in bacterial colony images.

      
 c) **ResNet50**:
 
    1) ResNets have demonstrated exceptional performance in computer vision tasks. By using both pre-trained and scratch-trained versions, we can evaluate the advantages of leveraging pre-trained knowledge and the challenges of working with a limited dataset in bacterial colony classification.
    
    2) Pre-trained ResNet50 offers faster convergence and potentially higher accuracy, which is valuable with limited data.

# Results
**K- means clustering**

![image](https://github.com/user-attachments/assets/51317326-c06e-4895-8ad0-8b385212e684)

K-means clustering for unsupervised learning on a dataset with four types of bacteria images, resulting in segmentation into four clusters.

![image](https://github.com/user-attachments/assets/82ed9f59-e937-43c2-89dc-b2dbebf2d0e4)

. Enhanced image dimensions improved clustering precision; employed PCA and t-SNE to visualize and understand the distribution of bacterial images in lower-dimensional spaces, revealing distinct clusters and intrinsic relationships.
  
. PCA and t-SNE reduced high-dimensional image data, enabling better insights into the separability and proximity of bacteria within the feature space.

**Vision Transformer** 

![image](https://github.com/user-attachments/assets/402a7c8f-5aad-4469-aef4-ad2533f06048)

1) Figure showing Accuracy and loss curves of ViT
2) As observed from the curves with ViT the accuracy is coming around 65%
3) The Vision Transformer model in this case had less accuracy comparatively as the data available is less. However it still proved to be an efficient architecture for 
   bacterial classification with images as it uses patch embedding and attention mechanism.

**ResNet50**

![image](https://github.com/user-attachments/assets/48d68782-92cd-411b-9edc-7e9135400664)

1) Figure showing Accuracy and loss curves of ResNet50
2) As observed from the curves with ResNet50 the accuracy is coming around 90%
3) After training the model, the model is tested on 100 images and the predictions are as follows:

![image](https://github.com/user-attachments/assets/f7147cbc-3087-40d8-aeee-b4199dff35c9)




