# MCANet: Multi-encoder Context Aggregation Network
This is an official site for MCANet model. Currently, we are uploading the output images and results here. Upon the acceptance of the paper, details will be provided.

## Datasets
For this research work, we have used Cityscapes, BDD100K and CamVid datasets.
* Cityscapes - To access this benchmark, user needs an account. https://www.cityscapes-dataset.com/downloads/ 
* BDD100K - To access this benchmark, user needs an account. https://doc.bdd100k.com/download.html     
* CamVid - To access this benchmark, visit this link: http://mi.eng.cam.ac.uk/research/projects/VideoRec/CamVid/

## Class mapping
Different datasets provide different class annotations. For instance, Camvid dataset has 32 class labels. Refer this link to know about all 32 classes of Camvid: http://mi.eng.cam.ac.uk/research/projects/VideoRec/CamVid/#ClassLabels. However, literature have shown that all the existing models are trained by 11 classes (Sky, Building, Pole, Road, Sidewalk, Tree, TrafficLight, Fence, Car, Pedestrian, Bicyclist) of Camvid dataset. Thereby, first 32 class annotations of Camvid are converted into 11 class annotations and then model is trained with 11 class annotations. To improve model performance, we also converted Cityscapes 19 class annotations to 11 class anotation and trained the model first with Cityscapes 11 class annotation, then use the pre-trained weight of Cityscapes to train the model with Camvid 11 class annotations. The following table shows the convertion of 32 classes of Camvid dataset to 11 classes.

TrainId | Camvid 11 classes  | Camvid 32 classes   
--------|--------------------|-------------------
   0    |        Sky         | Sky
   1    |     Building       | Archway, Bridge, Building, Tunnel, Wall
   2    |    Column_Pole     | Column_Pole, Traffic Cone
   3    |        Road        | Road, LaneMkgsDriv, LaneMkgsNonDriv  
   4    |      Sidewalk      | Sidewalk, ParkingBlock, RoadShoulder 
   5    |        Tree        | Tree, VegetationMisc
   6    |   TrafficLight     | TrafficLight, Misc_Text, SignSymbol  
   7    |       Fence        | Fence
   8    |        Car         | Car, OtherMoving, SUVPickupTruck, Train, Truck_Bus 
   9    |     Pedestrian     | Animal, CartLuggagePram, Child, Pedestrain   
  10    |     Bicyclist      | Bicyclist, MotorcycleScooter
  
  Note: Void class is not included in the set of 11 classes.
  
  The following table shows the mapping of Cityscapes 19 classes to Camvid 11 classes.
  
TrainId | Camvid 11 classes  | Cityscapes classes   
--------|--------------------|-------------------
   0    |        Sky         | Sky
   1    |     Building       | Building, Wall
   2    |    Column_Pole     | Pole, Polegroup
   3    |        Road        | Road  
   4    |      Sidewalk      | Sidewalk 
   5    |        Tree        | Vegetation
   6    |   TrafficLight     | Traffic Light, Traffic Sign  
   7    |       Fence        | Fence
   8    |        Car         | Car, Truck, Bus, Caravan 
   9    |     Pedestrian     | Person   
  10    |     Bicyclist      | Rider, Bicycle, MotorCycle


## Metrics
To understand the metrics used for model performance evaluation, please  refer here: https://www.cityscapes-dataset.com/benchmarks/#pixel-level-results

## Results
We trained our model by the above mentioned benchmarks at different input resolutions. Cityscapes provides 1024 * 2048 px resolution images. We mainly focus full resolution of cityscapes images. For CamVid dataset, we use 640 * 896 px resolution altough original image size is 720 * 960 px. Similarly, we use 768 * 1280 px resolution input images for BDD100K dataset although original size of input image is 720 * 1280 px. For Cityscapes and BDD100K datasets, we use 19 classes, however for Camvid dataset we trained the model with 11 classes (suggested by the literature). 

### Cityscapes test results
The output of the test set is submitted to Cityscapes evaluation server. To view the test set result evaluated by the server, click the following link: https://github.com/tanmaysingha/MCANet/blob/main/Cityscapes_test_results/Cityscapes_submission_results.pdf
Upon the acceptance of the paper, test results will be published in the Cityscapes evaluation server. Currently, serever provides the following anonymous link of our submission: https://www.cityscapes-dataset.com/anonymous-results/?id=b984f037a1dce36b8b74d3ee5de40378e170cf4be6641172071937a34f1b4fde


### Color map of Cityscapes dataset
![cityscapes_val_set](https://github.com/tanmaysingha/MCANet/blob/main/Figures/fig_cityscapes_color_map-eps-converted-to.pdf?raw=true)

### Prediction by different models on Cityscapes validation sample
![cityscapes_val_set](https://github.com/tanmaysingha/MCANet/blob/main/Figures/Cityscapes_val_predictions_new.png?raw=true)

### MCANet prediction on Cityscapes validation sample
![cityscapes_val_set](https://github.com/tanmaysingha/MCANet/blob/main/Figures/MCANet_val_prediction.png?raw=true)
  
### MCANet prediction on Cityscapes test samples
![Cityscapes_test_set](https://github.com/tanmaysingha/MCANet/blob/main/Figures/Cityscapes_test_predictions.png?raw=true)  

### Color map of CamVid dataset
![CamVid_val_set](https://github.com/tanmaysingha/MCANet/blob/main/Figures/camvid_color_map.png?raw=true)

### MCANet prediction on CamVid validation sample
![CamVid_val_set](https://github.com/tanmaysingha/MCANet/blob/main/Figures/Camvid_Val_MCANet.png?raw=true)

### Prediction by other models on CamVid validation sample
![CamVid_val_set](https://github.com/tanmaysingha/MCANet/blob/main/Figures/camvid_val_prediction_new.png?raw=true)

### MCANet prediction on CamVid test samples
![CamVid_test_set](https://github.com/tanmaysingha/MCANet/blob/main/Figures/camvid_test_predictions_new.png?raw=true)

### MCANet prediction on BDD100K validation sample
![BDD100K_val_set](https://github.com/tanmaysingha/MCANet/blob/main/Figures/BDD_val_predictions_new.png?raw=true)

### MCANet prediction on BDD100K test samples
![BDD100K_test_set](https://github.com/tanmaysingha/MCANet/blob/main/Figures/BDD_test_predictions_new.png?raw=true)
