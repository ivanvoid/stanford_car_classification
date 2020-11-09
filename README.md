# Stanford car classification
Car classification strategy for the course "Selected Topics in Visual Recognition using Deep Learning".  
For my approch **ACC: 0.93920**  

- [Summary](#summary-of-my-approach)
- [Reproducing](#reproducing-submission)
- [Hyperparameters](#hyperparameters)
- [Training](#training)
- [Test](#test)

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

## Training
For training just change hyperparameters on your own, and re-run notebook. 

## Test
You can put *k* models (k number of k-folds) in to *./models* folder and run notebook from [Test data prediction](https://render.githubusercontent.com/view/ipynb?commit=dd95090d915005bf0a007f5a07114456b2e16be6&enc_url=68747470733a2f2f7261772e67697468756275736572636f6e74656e742e636f6d2f766561782d766f69642f7374616e666f72645f6361725f636c617373696669636174696f6e2f646439353039306439313530303562663061303037663561303731313434353662326531366265362f43617225323064617461736574253230636c617373696669636174696f6e2e6970796e62&nwo=veax-void%2Fstanford_car_classification&path=Car+dataset+classification.ipynb&repository_id=311231378&repository_type=Repository#Test-data-prediction) part at the end of notebook.
