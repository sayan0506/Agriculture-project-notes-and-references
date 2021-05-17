# Agriculture-project-notes-and-references
Agriculture project notes and references

## Stage 1 Ground Survey

**[Ground Survey and Interactions with people involved in farming](https://github.com/sayan0506/Agriculture-project-notes-and-references/blob/main/Ground%20Survey.pdf)**

## Stage 2 Collecting possible ML proposals and ranking based on clarity, impact factor

**[ML_Solutions_Problems](https://docs.google.com/spreadsheets/d/1mgxP2OLr0P0VyUEZIh5kJLfJKdDNT26Pw5tVIWkwxsk/edit#gid=796617169)**

## Stage 3 Summarizing multiple ML solutions

**[Water Management System Proposal](https://github.com/sayan0506/Agriculture-project-notes-and-references/blob/main/Water%20Management%20Summarizations.pdf)**

**[Vision Plan](https://github.com/sayan0506/Agriculture-project-notes-and-references/blob/main/Satellite_vision_summary.pdf)**


## **Introduction:**

In agricultural field, everything is natural from production to maintenance of crops, weather effects, etc. and lots of uncertainities involved, which require continious and efficient monitoring, and take quick action in situation basis, which is not feasible for individuals, thus technology introduces it's vision for those solutions. There maybe severl vision based applications, when it comes to agriculture. Our goal is to bring multiple vision base applications under the same hood, so that we are proposing to make a centralized cloud based application, which is as follow:

### Centralized Cloud based Vision APP

#### System architecture:

***System 1.(Cloud based only with some seasonality)***

Application related to GIS, Satellite imagery based application. This section works in cloud and continuously monitor (or analyze on request) and analyze the satellite imagery, GIS data from satellites. Purpose and implementation:

Model deployment for 
•        Grazing pattern, Boundaries of crop
•        Crop-loss detection(accuracy is questionable using only satellite or GIS, need literature review)
•        Crop type detection(accuracy is questionable using only satellite or GIS, need literature review)
•        Missed fertilizer stripes
•        Farm-land area
•        Erosion detection
•        Water-body detection
•        Pest-detection(using GIS or satellite only here, but drone image for this purpose can be incorporated here)
•        Yield estimation

***System 2. (Cloud based but data fetching from real-world drone, farmers phone data)*** 

Application related to Drone imagery based application. This section works in cloud and continuously monitor (or analyze on request) and analyze the imagery and provides real-time response, Purpose and implementation:

Model deployment for
•        Vision based leaf disease stage detection(Pestiside spray based actuation, done by control node) 
•        Water-body detection(during drone survey with some routine-basis)
•        Real-time vision based crop, fruit health monitor(2d/3d mapping or image based strategy)
•        Plant stress classification
•        Real-time analysis of leaf or crop health from the uploaded image by farmers-friendly app. 
•        Crop, fruit count, quantity, type detection in real-time for crop or fruit collection in real-time.

***System 3.*** 

A. Mobile Apps for Farmers:

    Case a (Where no issue in Internet): 

    Farmers can upload images of crops, leafs etc. for obtaining real-time analytics based on real-time cloud program through their id, which can get real-time verification, 
    identification and recommended solution too.

    Case b (A real-time device having wireless connectivity with phones, can work without Internet):

    Farmers can upload images of crops, leafs etc. for obtaining real-time analytics based on real-time program  running on that master device in nearby operating units through     their id, which can get real-time verification, identification response, and recommended solution too.

B. Deployed Vision system in Drones or bots that are used in real-time while surveying

    1. Vision Unit(or say ROS node)
    
    Does all vision based applications mentioned above from analytics to precise image captures(regarding efficient homography estimation in real-time),[autonomous path planning     though out of scope here], deployed in the drone computer.
    
    2. Control unit

    Takes analytics result from vision node for actuating motors to conduct pitch, roll, yaw, and 
    from past analysis or the code involved for domain analysis to perform efficient, and precise
    application of following
    •        Herbiside spray
    •        Pestiside spray
    •        Watering or other necessary drone based application
   
   Note: Based on the application or purpose
   
   1. Drone can perform, image, analytics in real-time on-board, specially the actuation 
   based problem like spraying something in field.
   2. The drone can capture images only for crop type, area, boundary etc. analysis in 
   routine basis, this analytics application can be done later by a code running on cloud to
   save on-board battery power. 
   
#### ML Deployment reference   

* [TFX on Cloud AI Platform Pipelines](https://github.com/tensorflow/tfx/blob/master/docs/tutorials/tfx/cloud-ai-platform-pipelines.md)
* [Mobile Deep Learning with TFlite, ML kit and Flutter](https://drive.google.com/drive/folders/1TV3jpPnFbd4pxiVxxxEKxSsZibwUqoVo?usp=sharing), Use this for TFlite model conversion
* [Comparison Between Kubeflow and TFX](https://github.com/Future-AI-Laboratory/deployment-testing/blob/master/Comparison-Kubeflow-TFX.pdf)
* [TFX playlist](https://www.youtube.com/watch?v=YeuvR6m6ACQ&list=PLQY2H8rRoyvxR15n04JiW0ezF5HQRs_8F)
* [Using TensorFlow Extended (TFX) on AI Platform Pipelines live webinar](https://www.youtube.com/watch?v=RpWeVvAFzJE)
* [Using Kubeflow Pipelines on AI Platform, with Brian Kang along with git trigger](https://www.youtube.com/watch?v=qx7MLcbCo5g)
* [Continuous Deployment from git using Cloud Build | Cloud Run](https://cloud.google.com/run/docs/continuous-deployment-with-cloud-build)
* [How to Deploy a Machine Learning Model to Google Cloud for 20% Software Engineers (CS329s tutorial)](https://youtu.be/fw6NMQrYc6w)
* [Firebase Machine Learning BETA Machine learning for mobile developers](https://firebase.google.com/products/ml)
* [Image Augmentation on the fly using Keras ImageDataGenerator!](https://www.analyticsvidhya.com/blog/2020/08/image-augmentation-on-the-fly-using-keras-imagedatagenerator/)
* [Why and How to create requirements.txt](https://blog.usejournal.com/why-and-how-to-make-a-requirements-txt-f329c685181e)

#### References

1. **[CS 329S: Machine Learning Systems Design Stanford, Winter 2021](https://stanford-cs329s.github.io/syllabus.html)**
2. **[Stream Processing and Data Integration With Kafka in Cropin Agriculture](https://www.cropin.com/blogs/stream-processing-and-data-integration-with-kafka/)**
3. **[A Vision Based Method for Automatic Evaluation of Germination Rate of Rice Seeds](https://ieeexplore.ieee.org/document/8337511)**
4. **[CLAHE augmentations](https://www.kaggle.com/amritpal333/clahe-augmentation-ranzcr-comp)**
5. **[Irrigation Water Management](https://www.nrcs.usda.gov/Internet/FSE_DOCUMENTS/nrcs141p2_017781.pdf)**
6. **[Smart Water Management Technology and IoT](https://www.digiteum.com/smart-water-management-iot/#2)**
7. **[IRRIGATION WATER MANAGEMENT USING SMART CONTROL SYSTEMS: A REVIEW](https://www.researchgate.net/publication/329472758_IRRIGATION_WATER_MANAGEMENT_USING_SMART_CONTROL_SYSTEMS_A_REVIEW)**
8. **[EarthStat - GIS data for agriculture and the environment](http://www.earthstat.org/)**
9. **[Yield Estimation and Prediction](https://www.vista-geo.de/en/portfolio-items/yieldestimation/)**
10. **[Deep Learning for Plant Stress Phenotyping: Trends and Future Perspectives](https://www.sciencedirect.com/science/article/pii/S1360138518301572#fig0015)**
11. **[Using Geospatial Technology for Pest Monitoring and Detection](https://www.npdn.org/system/files/public/Meeting%20Information/2009_NationalMeeting/Kennaway_NPDN2009%20(3).pdf)**
12. **[Plant Disease Classification: A Comparative Evaluation of CNN models](https://www.mdpi.com/2223-7747/9/10/1319/pdf#:~:text=The%20Xception%20model%20attained%20the,disease%20on%20the%20PlantVillage%20dataset)**
13. **[Plant Disease Classification: A Comparative Evaluation of Convolutional Neural Networks and Deep Learning Optimizers](https://www.mdpi.com/2223-7747/9/10/1319/pdf#:~:text=The%20Xception%20model%20attained%20the,disease%20on%20the%20PlantVillage%20dataset)**
14. **[Xception-PyTorch](https://github.com/tstandley/Xception-PyTorch)**
15. **[Review: Xception — With Depthwise Separable Convolution](https://towardsdatascience.com/review-xception-with-depthwise-separable-convolution-better-than-inception-v3-image-dc967dd42568?gi=224ea57f354)**
16. **[Weed detection and segmentation](https://github.com/Midnight93/Weeds-Detection-and-Segmentation)**
17. **[Leaf-image-segmentation](https://github.com/YaredTaddese/leaf-image-segmentation)**
18. **[Deep Learning-Based Segmentation and Quantification of Cucumber Powdery Mildew Using Convolutional Neural Network](https://www.frontiersin.org/articles/10.3389/fpls.2019.00155/full)**
19. **[Leaf-net Implementation](https://github.com/deepakHonakeri05/Leaf-Disease-Classifier)**
20. **[Deep Learning for the plant disease detection](https://github.com/MarkoArsenovic/DeepLearning_PlantDiseases)**
21. **[Plant Diseases Detector](https://github.com/Oskop/Pladiator)**
22. **[Comparative Assessment of Deep Learning to Detect the Leaf Diseases of Potato based on Data Augmentation](https://github.com/sayan0506/Agriculture-project-notes-and-references/blob/main/Potato%20classification%20model%20CNN.pdf)**
23. **[Rice Leaf Disease Classification using CNN](https://www.researchgate.net/publication/348243112_Rice_Leaf_Diseases_Recognition_Using_Convolutional_Neural_Networks)**
24. **[Grape Leaf Disease Classification Using Improved Deep CNN](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7373759/pdf/fpls-11-01082.pdf)**
25. **[Plant diseases and pests detection based on deep learning: a review](https://data.mendeley.com/datasets/s62zm6djd2/1)**
26. **[Application of Deep Learning in Integrated Pest Management: A Real-Time System for Detection and Diagnosis of Oilseed Rape Pests](https://downloads.hindawi.com/journals/misy/2019/4570808.pdf)**
27. **[An optimized dense convolutional neural network model for disease recognition and classification in corn leaf](https://www.sciencedirect.com/science/article/abs/pii/S0168169920302180?via%3Dihub)**
28. **[Live AWS For Data Science - Deploying Machine Learning Application In EC2 Instance](https://youtu.be/kQ9qiIzsFxM)**
29. **[Continuous deployment from Git using Cloud Build](https://cloud.google.com/run/docs/continuous-deployment-with-cloud-build)**
30. **[How to Deploy a Machine Learning Model to Google Cloud for 20%](https://youtu.be/fw6NMQrYc6w)**
31. **[Identification of Tomato Leaf Disease Detection using Pretrained Deep Convolutional Neural Network Models](https://www.scpe.org/index.php/scpe/article/view/1780)**
