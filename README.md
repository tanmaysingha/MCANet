# MCANet: Multi-encoder Context Aggregation Network
This is an official site for MCANet model. Currently, we are uploading the output images and results here. Upon the acceptance of the paper, details will be provided.

## Datasets
For this research work, we have used Cityscapes, BDD100K and CamVid and BDD100K datasets.
* Cityscapes - To access this benchmark, user needs an account. https://www.cityscapes-dataset.com/downloads/ 
* BDD100K - To access this benchmark, user needs an account. https://doc.bdd100k.com/download.html     
* CamVid - To access this benchmark, visit this link: http://mi.eng.cam.ac.uk/research/projects/VideoRec/CamVid/

## Metrics
To understand the metrics used for model performance evaluation, please  refer here: https://www.cityscapes-dataset.com/benchmarks/#pixel-level-results

## Results
We trained our model by the above mentioned benchmarks at different input resolutions. Cityscapes provides 1024 * 2048 px resolution images. We mainly focus full resolution of cityscapes images. For CamVid dataset, we use 640 * 896 px resolution altough original image size is 720 * 960 px. Similarly, we use 768 * 1280 px resolution input images for BDD100K dataset although original size of input image is 720 * 1280 px. For Cityscapes and BDD100K datasets, we use 19 classes, however for Camvid dataset we trained the model with 11 classes (suggested by the literature). 

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
