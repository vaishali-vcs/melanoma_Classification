# melanoma_Classification
Data Source- https://www.kaggle.com/c/siim-isic-melanoma-classification


| Experiment | Model Inputs | Image Augmentation |Model Chosen | Hyperparameters |LB Score |
| :---:         |       ---: | :---       | :---         |     :---:      |          ---: |
|  <p align="left">TPU</p>   |   <p align="left">Metadata & Images(384X384)</p> | <p align="left">randomly flip image left/right & up/down<br>randomly set hue<br>randomly set saturation<br>randomly set contrast<br>randomly set brightness<br>data CutMix</p>| <p align="left">EfficientNetB3</p> | <p align="left">LR= 1e-3<br>loss=Focal Loss<br>epochs= 15<br>Batch Size=16</p> |  0.8856  |
|  <p align="left">AutoML + vgg16 attention</p>   |  <p align="left">Metadata & Images(512X512)</p> | <p align="left">Rotate images by 10 degrees<br>reverse 50% of Train<br>Resize<br>Normalize<br>CenterCrop<br>Random Rotation & Horizontal Flip</p> | <p align="left">XGB & vgg16 with attention</p> | <p align="left">LR=1e-4<br> loss=Focal Loss</p> |0.9395  |
|  <p align="left">EfficientNet B6, B7 ensemble</p> | <p align="left">Only Images(256x256)</p> | <p align="left">Rotation<br>Translation<br>Shear<br>Zoom</p> | <p align="left">EfficientNet B6, B7</p> | <p align="left">epochs=13</p> | 0.9337 |
|  <p align="left">EfficientNet B0-B7 ensemble   |  <p align="left">Only Images</p> | <p align="left">hyperparams</p> |  <p align="left">Ensemble of following models:  EfficientNet B0, B1, B2, B3, B4, B5, B6,B7</p> |  <p align="left">params</p> | 0.9330 |
