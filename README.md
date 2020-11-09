# Stanford car classification
Car classification strategy for the course "Selected Topics in Visual Recognition using Deep Learning".  
For my approch **ACC: 0.93920**  

- [Summary](#summary-of-my-approach)
- [Reproducing](#reproducing-submission)
- [Hyperparameters](#hyperparameters)
- [Training]()
- [Test]()

## Summary of my approach
Train different models on k-fold cross validation with varius augmintations.  
Then use those models for predicting test data using Test time augmintation starategy, take mean of their predictions and submit it.

## Reproducing Submission  
To reproduct my submission without retrainig, do the following steps:
- Run all cells exept train cell.

## Hyperparameters
|Parameter|Meaning|Value|
|---|---|---|
|image_size|Size for image resizing|(244,244)|
|seed|Seed for random setup|69|
|batch_size|Batch size for model training|44|
|k_folds|Number of folds for crossvalidation|5|
|n_epochs|Number of training epochs|40|
|MODEL_NAME|Name of the model from Efficientnet family|'efficientnet-b2'|
|lr|learning rate for SGD|0.001|
|max_lr|max_lr for OneCycle scheduler|0.1|
|n_TTA|Number of Test Time Augmentations, must be even, because we have one unaugmented prediction.|8|
|device|Device for computation|'cuda'|
