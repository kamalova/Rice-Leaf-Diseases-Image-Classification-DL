![banner](https://github.com/kamalova/Rice_Leaf_Disease_Recognition_DL/blob/main/Images/banner.jpg)
<div align="center"><img src="https://github.com/kamalova/Rice_Leaf_Disease_Recognition_DL/blob/main/Images/banner_2.png"</img> </div>

## **Rice Leaf Disease Image Classification Using Deep Learning**
**Author: Nurgul Kurbanali kyzy** <p>
#### Table of Contents
* [Overview and Business Statement](https://github.com/kamalova/Rice_Leaf_Disease_Img_Classification_DL/blob/main/README.md#overview-and-business-statement)
* [Data Understanding](https://github.com/kamalova/Rice_Leaf_Disease_Img_Classification_DL#data-understanding)
* [Model Analysis](https://github.com/kamalova/Rice_Leaf_Disease_Img_Classification_DL#model-analysis)
* [Conclusion](https://github.com/kamalova/Rice_Leaf_Disease_Img_Classification_DL#conclusion-)
* [Recommendations and Future Consideration](https://github.com/kamalova/Rice_Leaf_Disease_Img_Classification_DL#recommendations-and-future-consideration)
* [For More Information](https://github.com/kamalova/Rice_Leaf_Disease_Img_Classification_DL#for-more-information)

###  Overview and Business Statement 
Rice is one of the most cultivated crops in the world, in over a hundred countries. Rice production is the 3rd largest among cereals in the U.S. Arkansas where our stakeholders from ranks 1st in rice production in the U.S., accounting for over 40% of rice production.With rice being such a valuable commodity, a common problem that widespread cultivators face is infestation of rice leaf diseases. Infection by diseases results in great loss to economic to the farmers in every year.

In traditional practices, identification is performed either by visual observation or by testing in laboratory. The visual observation requires expertise and it may vary subject to an individual which may lead to an error while the laboratory test is time consuming and may not be able to provide the results in time. Taking into consideration the large range of possible diseases, it becomes a difficult task for cultivators to individually identify these cases, especially for large fields. 
  
In an effort to solve this problem and assist farmers and everyday gardeners to ensure a healthy crop, *Leaf Green* uses an image classification model to help predict and identify three common leaf diseases (Brown Spot, Leaf Blast) along with Healthy plants based on 3355 rice images
  
### Data Understanding
 The data was sourced from https://www.kaggle.com/datasets/nizorogbezuode/rice-leaf-images dataset . The images are in 4 folders, classified as follows:<p>
 ![class_distr](https://github.com/kamalova/Rice_Leaf_Disease_Recognition_DL/blob/main/Images/class_distribution.png) <p>
 
  Natural Green leaves indicate **Healthy** rice plants.
  ![healthy](https://github.com/kamalova/Rice_Leaf_Disease_Recognition_DL/blob/main/Images/health.png) <p>
 **Leaf Blast** *(leaf and collar)* is caused by the fungus Magnaporthe oryzae. It can affect all above ground parts of a rice plant: leaf, collar, node, neck, parts of panicle, and sometimes leaf sheath. Rice can have blast in all growth stages.
  ![lb](https://github.com/kamalova/Rice_Leaf_Disease_Recognition_DL/blob/main/Images/lb.png) <p>
 **Hispa** scrapes the upper surface of leaf blades leaving only the lower epidermis. It also tunnels through the leaf tissues. When damage is severe, plants become less vigorous. The presence of grassy weeds in and near rice fields as alternate hosts harbor and encourage the pest to develop. <p>
  ![hispa](https://github.com/kamalova/Rice_Leaf_Disease_Recognition_DL/blob/main/Images/hispa.png) <p>
 **Brown Spot**  *(Helminthosporiose)* is the one of the major fungal diseases in rice in which it is caused by Bipolarisoryzae. The fungus can survive in the seed for more than four years and can spread from plant to plant through air.
  ![bs](https://github.com/kamalova/Rice_Leaf_Disease_Recognition_DL/blob/main/Images/bs.png) <p>

  
### Model Analysis
After modeling with various CNN's the most promising involved transfer learning with *InceptionV3*. 
This model was announced by the Google team in December 2015. V2 has two 3x3 convolution kernels instead of a 5x5, while V3 will decompose more thoroughly. The core idea of V3 is to first use two 3x3 convolution kernels instead of 5x5 convolution kernels, and three 3x3 convolution kernels instead of 7x7 convolution kernels to reduce the amount of parameters and speed up calculations. V3 further decomposes the nxn convolution kernel into 1xn and nx1 convolution kernels, while reducing the size of the feature map and increasing the number of channels.
### Conclusion <p>
   ![classf_report](https://github.com/kamalova/Rice_Leaf_Disease_Recognition_DL/blob/main/Images/classif_report.png) <p> 
The advantages of an automated rice disease detection system can prove of much value to agricultural organizations and cultivators. Based on the evaluation of the test set **Leaf Green** can be expected to correctly class new images around 79% accuracy.<p> 
   ![barplot](https://github.com/kamalova/Rice_Leaf_Disease_Recognition_DL/blob/main/Images/barplot.png) <p> 
*Brown Spot* - performed predictions of true values (TP) at 77%. However, it has false alarms at 23% with other three classes.<p>
*Healthy* - performed almost perfect job at 92% with the true values (TP). It has 6% false alarms on hispa and leaf blast. Misclassification rate is 1% with brown spot.<p>
*Leaf Blast*- Performed correct prediction with 72% which  nearly same as brown spot(less 5%). It misclassified 26% with healthy and hispa leaves.<p>
*Hispa* - performing one of the worst according to our normalized confusion matrix. It did classify 39% of the leaves as a healthy ones which is bad for disease prevention.<p>
### Recommendations and Future Consideration
*Leaf Green* can be used to classify two common diseases(brown spot, leaf blast) along with healthy rice leaves. We recommend to use this product as early as possible to catch disease before it spreads to the rest of the rice plants.<p>
In terms of hispa disase model did strugle to classify it correctly. It may be due to the image quality. They may have a lot in common with regular healthy leaves so model classified them as a healthy ones. This class needs to be further improved with more and diverse image datasets s along with other common disease.<p>
Experimenting with a different algorithm and adding some context to the data may also lead to some improvements.<p>
Based on the achieved results a mobile solution (application) can be developed for farmers and agricultural organizations to detect rice leaf diseases at hand.<p>
Adding location data to the model would be helpful for users as some diseases are more common in certain climates.<p>
 
### For More Information
You can review my full analysis in my [Jupyter Notebook](https://github.com/kamalova/Rice_Leaf_Disease_Recognition_DL/blob/main/notebook.ipynb) or my [presentation](https://github.com/kamalova/Rice_Leaf_Disease_Recognition_DL/blob/main/PDFs/presentation.pdf).<p>
For any additional questions, please contact Nurgul Kurbanali kyzy at nurkamalova@gmail.com<p>
**Repository Structure**

  
  
