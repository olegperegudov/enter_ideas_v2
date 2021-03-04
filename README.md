# Project overview:

- Dataset used: https://www.kaggle.com/gobsan/st-george-or-not
- Dataset description: binary classification of ~6000 pics with St. George.
- This NB attempts to classify a given dataset with Saint George using Pytorch and a pretrained resnet50 model. No extra images were added to the dataset.

This is what was done:

Prep work included using Pandas for path and label collection of all data.
1. The data was split into train, valid and test datasets.
2. Some minor augmentations added to the data.
3. The model was 1st trained with all but the last layer frozen for a couple of epochs, then all params were unfrozen and the whole model trained again.
4. tta was used on test dataset.

The model shows signs of overfitting the train set, but valid and, most importantly, test set error rates are good indicators of the model is working properly.

## How to run:

- Easiest would be to make a copy and run it directly on kaggle.com - https://www.kaggle.com/gobsan/enter-ideas-george-torch
- This way it will have all the needed dependencies and dataset preinstalled
