# MCANet: Multi-encoder Context Aggregation Network
This is an official site for MCANet model. Currently, we are uploading the output images and results here. Upon the acceptance of the paper, details will be provided.

## Datasets
For this research work, we have used Cityscapes, BDD100K and CamVid datasets.
* Cityscapes - To access this benchmark, user needs an account. https://www.cityscapes-dataset.com/downloads/ 
* BDD100K - To access this benchmark, user needs an account. https://doc.bdd100k.com/download.html     
* CamVid - To access this benchmark, visit this link: http://mi.eng.cam.ac.uk/research/projects/VideoRec/CamVid/

## Class mapping
Different datasets provide different class annotations. For instance, Camvid dataset has 32 class labels: Animal, Archway, Bicyclist, Bridge, Building, Car, CartLuggagePram, Child, Column_Pole, Fence, LaneMkgsDriv, LaneMkgsNonDriv, Misc_Text, MotorcycleScooter, OtherMoving, ParkingBlock, Pedestrian, Road, RoadShoulder, Sidewalk, SignSymbol, Sky, SUVPickupTruck, TrafficCone, TrafficLight, Train, Tree, Truck_Bus, Tunnel, VegetationMisc, Void, Wall. However, literature have shown that out of 32 classes, all the existing models are trained by 11 classes: Sky, Building, Pole, Road, Sidewalk, Tree, TrafficLight, Fence, Car, Pedestrian, Bicyclist. Thereby, first 32 class annotations of Camvid are converted to 11 class annotations and then model is trained with 11 class annotations. To improve model performance, we also converted Cityscapes 19 class annotations to 11 class anotation and trained the model first with Cityscapes 11 class annotation, then use the pre-trained weight of Cityscapes to train the model with Camvid 11 class annotations. The following table shows class mapping between Cityscapes and Camvid dataset.

TrainId | Cityscapes classes | Camvid classes   
--------|--------------------|------------------
   0    |        Sky         |  Sky
   1    |      Building      | Building
   2    |      Building      | Pole
   3    |        Wall        |  Road 
   4    |       Fence        |  Sidewalk 
   5    |        Pole        | Tree
   6    |   Traffic light    | TrafficLight  
   7    |   Traffic sign     | Fence
   8    |    Vegetation      | Car 
   9    |      Terrain       | Pedestrain   
  10    |        Sky         | Bicyclist 
  11    |      Person        |  
  12    |       Rider        |   Rider
  13    |        Car         |   
  14    |      Truck         |  Truck
  15    |        Bus         |   Bus
  16    |      Train         |  Train
  17    |    Motorcycle      | Motorcycle
  18    |      Bicycle       |  Bicycle


## Metrics
To understand the metrics used for model performance evaluation, please  refer here: https://www.cityscapes-dataset.com/benchmarks/#pixel-level-results

## Results
We trained our model by the above mentioned benchmarks at different input resolutions. Cityscapes provides 1024 * 2048 px resolution images. We mainly focus full resolution of cityscapes images. For CamVid dataset, we use 640 * 896 px resolution altough original image size is 720 * 960 px. Similarly, we use 768 * 1280 px resolution input images for BDD100K dataset although original size of input image is 720 * 1280 px. For Cityscapes and BDD100K datasets, we use 19 classes, however for Camvid dataset we trained the model with 11 classes (suggested by the literature). 

### Cityscapes test results
The output of the test set is submitted to Cityscapes evaluation server. To view the test set result evaluated by the server, click the following link: https://github.com/tanmaysingha/MCANet/blob/main/Cityscapes_test_results/Cityscapes_submission_results.pdf
Upon the acceptance of the paper, we will publish the results in Cityscapes leader-board.

### MCANet prediction on Cityscapes validation sample
![cityscapes_val_set](https://github.com/tanmaysingha/MCANet/blob/main/Figures/MCANet_val_prediction.png?raw=true)
  
### MCANet prediction on Cityscapes test samples
![Cityscapes_test_set](https://github.com/tanmaysingha/MCANet/blob/main/Figures/Cityscapes_test_predictions.png?raw=true)  

### MCANet prediction on CamVid validation sample
![CamVid_val_set](https://github.com/tanmaysingha/MCANet/blob/main/Figures/Camvid_Val_MCANet.png?raw=true)

### MCANet prediction on CamVid test samples
![CamVid_test_set](https://github.com/tanmaysingha/MCANet/blob/main/Figures/camvid_test_predictions.png?raw=true)

### MCANet prediction on BDD100K validation sample
![BDD100K_val_set](https://github.com/tanmaysingha/MCANet/blob/main/Figures/BDD_Val_MCANet.png?raw=true)

### MCANet prediction on BDD100K test samples
![BDD100K_test_set](https://github.com/tanmaysingha/MCANet/blob/main/Figures/BDD_test_predictions.png?raw=true)
