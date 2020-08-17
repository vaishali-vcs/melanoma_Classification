# melanoma_Classification
Data Source- https://www.kaggle.com/c/siim-isic-melanoma-classification


| Experiment | Model Inputs | Image Augmentation |Model Chosen | Hyperparameters |LB Score |
| :---:         |       ---: | :---       | :---         |     :---:      |          ---: |
|  <p align="left">TPU</p>   |   <p align="left">Metadata & Images</p> | | <p align="left">EfficientNetB3 | <p align="left">LR=0.0001<br>loss=Focal Loss</p> |  0.8856  |
|  <p align="left">AutoML + vgg16 attention</p>   |  <p align="left">Metadata & Images</p> | |  <p align="left">XGB & vgg16 with attention</p>|  <p align="left">Maximum character sequence considered=128</p>|  0.9395  |
|  <p align="left">EfficientNet B6, B7 ensemble     |   <p align="left">Only Images</p> |  |  <p align="left">EfficientNet B6,B7 |  <p align="left">Maximum character sequence considered=160 |  0.9337 |
|  <p align="left">EfficientNet B0-B7 ensemble   |  <p align="left">Only Images</p> | |  <p align="left">Ensemble of following models:  EfficientNet B0, B1, B2, B3, B4, B5, B6,B7</p> |  <p align="left">Maximum character sequence considered=512 SVM: kernel='rbf',gamma='auto', MLP: Dense and Sigmoid with two Conv1D & MaxPool layers, Number of epochs = 5, batch_size=16,Learning Rate=2e-6</p> | 0.9330 |
