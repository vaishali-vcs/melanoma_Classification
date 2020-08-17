# melanoma_Classification
Data Source- https://www.kaggle.com/c/siim-isic-melanoma-classification


| Experiment | Feature Engineering |Model Chosen | Hyperparameters |Leaderboard Score |
| :---:         |       ---: | :---         |     :---:      |          ---: |
| TPU   | Removed Emoji, urls and non-ASCII characters, punctuations. 16 Targets that were misclassified were corrected. |EfficientNetB3 | Maximum character sequence considered=128|  0.8353  |
| AutoML + vgg16 attention   | Removed Emoji, urls and non-ASCII characters, punctuations. 16 Targets that were misclassified were corrected. | XGB & vgg16 attention| Maximum character sequence considered=128|  0.8353  |
| EfficientNet B6,B7 ensemble     | Abbreviations such as ppl, nyc, etc were replaced. None of targets corrected.|  EfficientNet B6,B7 | Maximum character sequence considered=160 |  0.8404 |
| EfficientNet B0-B7 ensemble   | Converted text to lowercase. Removed hashtags, usernames, links and usernames. Added features- number of hashtags, usernames, links, mentions. |Ensemble of following models:  EfficientNet B0, B1, B2, B3, B4, B5, B6,B7| Maximum character sequence considered=512 SVM: kernel='rbf',gamma='auto', MLP: Dense and Sigmoid with two Conv1D & MaxPool layers, Number of epochs = 5, batch_size=16,Learning Rate=2e-6 | 0.8312 |
