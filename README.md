# Project overview:

- Dataset used: https://www.kaggle.com/gobsan/st-george-or-not
- Dataset description: binary classification of ~6000 pics with St. George.
- This NB attempts to classify a given dataset with Saint George using Pytorch and a pretrained resnet50 model. No extra images were added to the dataset.

This is what was done:

1. Prep work included using Pandas for path and label collection of all data.
2. The data was split into train, valid and test datasets.
3. Some minor augmentations added to the data.
4. The model was 1st trained with all but the last layer frozen for a couple of epochs, then all params were unfrozen and the whole model trained again.
5. TTA was used on test dataset.
6. I could get ~6.5% error rate with 3 frozen and ~10 unfozen epochs.

The model shows signs of overfitting the train set, but valid and test set error rates are good indicators of the model working properly.

## How to run:

1. Easiest would be to make a copy and run it directly on kaggle.com - https://www.kaggle.com/gobsan/enter-ideas-george-torch
This way it will have all the needed dependencies and dataset preinstalled.
Just turn on GPU acceleration and run the whole thing. It will take ~ 15-20 min if you run it as is.

2. You can also run inference NB only. With no training required, you can see it at: https://www.kaggle.com/gobsan/enter-ideas-george-torch-inference
Just copy & edit it to open. Then "run all". It shouldn't take more than a few seconds for result to pop up. Can run CPU or GPU. You can try to classify a few images yourself providing URL.

3. You can try and run it locally with Jupyter NB if you have GPU available, but you will also need to set up paths to your files and the dataset itself (can be DL from kaggle). I only had CPU and there were some problems running it this way (couldn't check how it runs with GPU locally). Even after installing all the dependencies from requirements file.
