# melanoma_Classification
Data Source- https://www.kaggle.com/c/siim-isic-melanoma-classification


| Experiment | Model Inputs | Image Augmentation |Model Chosen | Hyperparameters |LB Score |
| :---:         |       ---: | :---       | :---         |     :---:      |          ---: |
| TPU   |  Metadata & Images | |EfficientNetB3 | LR=0.0001<br>loss=Focal Loss |  0.8856  |
| AutoML + vgg16 attention   | Metadata & Images | | XGB & vgg16 with attention| Maximum character sequence considered=128|  0.9395  |
| EfficientNet B6,B7 ensemble     |  Only Images |  | EfficientNet B6,B7 | Maximum character sequence considered=160 |  0.9337 |
| EfficientNet B0-B7 ensemble   | Only Images| | Ensemble of following models:  EfficientNet B0, B1, B2, B3, B4, B5, B6,B7| Maximum character sequence considered=512 SVM: kernel='rbf',gamma='auto', MLP: Dense and Sigmoid with two Conv1D & MaxPool layers, Number of epochs = 5, batch_size=16,Learning Rate=2e-6 | 0.9330 |
