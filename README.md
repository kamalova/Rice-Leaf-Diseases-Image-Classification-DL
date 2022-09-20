![banner](https://github.com/kamalova/Rice_Leaf_Disease_Recognition_DL/blob/main/Images/banner.jpg)
# **LEAF**![](https://github.com/kamalova/Rice_Leaf_Disease_Recognition_DL/blob/main/Images/logo.jpg)**GREEN**  
## **Rice Plant Disease Recognition Using Deep Learning**
**Author: Nurgul Kurbanali kyzy** <p>
#### Table of Contents
* [Overview and Business Statement](https://github.com/kamalova/Rice_Leaf_Disease_Recognition_DL/blob/main/README.md#overview-and-business-statement)
* [Data Understanding](https://github.com/kamalova/Rice_Leaf_Disease_Recognition_DL/blob/main/README.md#overview-and-business-statement)
* [Model Analysis](https://github.com/kamalova/Rice_Leaf_Disease_Recognition_DL/blob/main/README.md#overview-and-business-statement)
* [Conclusion](https://github.com/kamalova/Rice_Leaf_Disease_Recognition_DL/blob/main/README.md#overview-and-business-statement)
* [Recommendations and Future Consideration](https://github.com/kamalova/Rice_Leaf_Disease_Recognition_DL/blob/main/README.md#overview-and-business-statement)
* [For More Information]

###  Overview and Business Statement 
Rice is one of the most cultivated crops in the world, in over a hundred countries. As per reports by interest groups, rice consists of a total harvested area of approximately 158 million hectares, producing more than 700 million tons annually (470 million tons of milled rice). With rice being such a valuable commodity, a common problem that widespread cultivators face is infestation of rice leaf diseases. Infection by diseases results in great loss to economic to the farmers in every year.

In traditional practices, identification is performed either by visual observation or by testing in laboratory. The visual observation requires expertise and it may vary subject to an individual which may lead to an error while the laboratory test is time consuming and may not be able to provide the results in time. Taking into consideration the large range of possible diseases, it becomes a difficult task for cultivators to individually identify these cases, especially for large fields. 
  
In an effort to solve this problem and assist farmers and everyday gardeners to ensure a healthy crop, **Leaf Green** uses an image classification model to help predict and identify three common leaf diseases  *(Brown Spot, Leaf Blast, Hispa)*  based on images of both healthy and diseased rice plant leaves.
  
### Data Understanding
 The data was sourced from https://www.kaggle.com/datasets/nizorogbezuode/rice-leaf-images dataset . The images are in 4 folders, classified as follows:<p>
 ![class_distr](https://github.com/kamalova/Rice_Leaf_Disease_Recognition_DL/blob/main/Images/class_distribution.png) <p>
  
  Natural Green leaves indicate **Healthy** rice plants.
  ![healthy](https://github.com/kamalova/Rice_Leaf_Disease_Recognition_DL/blob/main/Images/health.png) <p>
 **Leaf Blast** *(leaf and collar)* is caused by the fungus Magnaporthe oryzae. It can affect all above ground parts of a rice plant: leaf, collar, node, neck, parts of panicle, and sometimes leaf sheath. Rice can have blast in all growth stages.
  ![lb](https://github.com/kamalova/Rice_Leaf_Disease_Recognition_DL/blob/main/Images/lb.png) <p>
 **Hispa** scrapes the upper surface of leaf blades leaving only the lower epidermis. It also tunnels through the leaf tissues. When damage is severe, plants become less vigorous. The presence of grassy weeds in and near rice fields as alternate hosts harbor and encourage the pest to develop. <p>
  ![hispa](https://github.com/kamalova/Rice_Leaf_Disease_Recognition_DL/blob/main/Images/hispa.png) <p>
 **Brown Spot)**  *(Helminthosporiose)* is the one of the major fungal diseases in rice in which it is caused by Bipolarisoryzae. The fungus can survive in the seed for more than four years and can spread from plant to plant through air.
  ![bs](https://github.com/kamalova/Rice_Leaf_Disease_Recognition_DL/blob/main/Images/bs.png) <p>

  
### Model Analysis
After modeling with various CNN's the most promising involved transfer learning with *InceptionV3*. 
This model was announced by the Google team in December 2015. V2 has two 3x3 convolution kernels instead of a 5x5, while V3 will decompose more thoroughly. The core idea of V3 is to first use two 3x3 convolution kernels instead of 5x5 convolution kernels, and three 3x3 convolution kernels instead of 7x7 convolution kernels to reduce the amount of parameters and speed up calculations. V3 further decomposes the nxn convolution kernel into 1xn and nx1 convolution kernels, while reducing the size of the feature map and increasing the number of channels.
### Conclusion <p>
The advantages of an automated rice disease detection system can prove of much value to agricultural organizations and cultivators. Based on the evaluation of the test set **Leaf Green** can be expected to correctly class new images around 79% accuracy.<p> The confusion matrix from the test set is depicted below. The model is much better at correctly identifying the healthy leaves, and still struggles with correctly identifying the hispa leaves. However, it is overall predicting most of each class correctly.<p>
   ![conf_matrix](https://github.com/kamalova/Rice_Leaf_Disease_Recognition_DL/blob/main/Images/conf_matrix.png) <p> 
   ![classf_report](https://github.com/kamalova/Rice_Leaf_Disease_Recognition_DL/blob/main/Images/classif_report.png) <p> 
### Recommendation and Future Consideration
**LEAF**![](https://github.com/kamalova/Rice_Leaf_Disease_Recognition_DL/blob/main/Images/logo.jpg)**GREEN** 
 can be trusted to properly class common rice leaf diseases. We recommend to use this product as early as possible to catch disease before it spreads to the rest of the rice plants.<p>
* The performance of proposed model can be further improved with large dataset of rice diseased images along with other common disease.
* Based on the achieved results a mobile solution (application) can be developed for farmers and agricultural organizations to detect rice leaf diseases at hand. <p>
* Adding location data to the model would be helpful for users as some diseases are more common in certain climates.<p>
  
### For More Information
You can review my full analysis in my Jupyter Notebook or my presentation.<p>
For any additional questions, please contact Nurgul Kurbanali kyzy at nurkamalova@gmail.com<p>

Repository Structure
