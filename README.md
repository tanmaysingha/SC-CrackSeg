
# SC-CrackSeg: A Real-time Shared Feature Pyramid Network for Crack Detection and Segmentation
This is an official site for SC-CrackSeg. It is a real-time crack detection and segmentation model. The performanc of this model is evaluated on Crack datasets, available at Kaggle data science community. This dataset merges 12 different crack segmentation datasets. It provides 9,505 training images and 1,695 test. The size of each image is 448 x 448 px. Currently, the model predictions and supplimentary materials are uploaded. Upon the acceptance of the paper, this repository will be updated.

## Datasets
* Crack datasets - extracted from the Kaggle data science community: https://www.kaggle.com/ 

## Network architecture
The backbone design of SC-CrackSeg is motivated by the design of SCMNet model. It uses a knowledge shared backbone for feature extraction. The complete pipeline of SC-CrackSeg is displayed in the following figure.

![pipeline](https://github.com/tanmaysingha/SC-CrackSeg/blob/main/Images/CrackSeg-pipeline.png?raw=true)

## Performance metrics
As the goal of this model is detecting and segmenting crack from the scene, hence we use mean Intersection Over Union (mIoU) metric for semantic performance evaluation. Apart from that, other necessary metrics such as Precision, recall and accuracy are also explored and measured. Due to the highly imbalanced class distribution, the F1, precision and recall metrics are more useful than the accuracy metric.

## Results
We trained our model by the above mentioned benchmarks at different input resolutions. For Cityscapes and KITTI datasets, we use 19 classes, however for Camvid dataset we trained the model with 11 classes (suggested by the literature). The following table exhibits the test results achieved by SDBNet.

Accuracy |   mIoU   |   mF1   |   mAP   |   mRC   | No. of parameters | FLOPs |  FPS    
---------|----------|---------|---------|---------|-------------------|-------|-------
 98.52%  |  77.04%  |  85.34% |  88.59% |  82.32% |   1.24 million    | 2.8 G |  220
--------------------------------------------------------------------------------------

### Sample Annotation

![annotation](https://github.com/tanmaysingha/SC-CrackSeg/blob/main/Images/annotation1.png?raw=true)

### Prediction by different models

![Output_by_all](https://github.com/tanmaysingha/SC-CrackSeg/blob/main/Images/output.png?raw=true)
 
### Prediction by SC-CrackSeg using different crack datasets samples

![Output_by_SCCrackSeg](https://github.com/tanmaysingha/SC-CrackSeg/blob/main/Images/model_predictions.png?raw=true)  

 ### Citation
 ```yaml
cff-version: 1.2.0
If this research work is useful for your research work, then please consider for citing the paper:
  @INPROCEEDINGS{crackSeg2022singha,
  author={Singha, Tanmay and Bergemann, Moritz and Pham, Duc-Son and Krishna, Aneesh},
  booktitle={Proc. DICTA}, 
  title={{SC-CrackSeg: A Real-time Shared Feature Pyramid Network for Crack Detection and Segmentation}}, 
  year={2022},
  volume={},
  number={},
  pages={1-8},
  doi={10.1109/DICTA56598.2022.10034629}}

```
