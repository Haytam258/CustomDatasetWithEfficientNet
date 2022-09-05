# CustomDatasetWithEfficientNet

In this mini-project, we're making our own dataset from Kaggle's Food101 (a set that has 101 classes, with 1000 images per class).

It'll be made of 3 classes instead: Pizza, Sushi and Steak

We'll apply some image transformations using the Torchvision `transforms` in order to modify our images as well as `TrivialAugmentWide()` to do data augmentation (although it's mostly used in order to avoid overfitting)

Then, we'll build our TinyVGG model and train it on a non-augmented dataset and an augmented dataset.

Finally, we'll use transfer learning in order to use a pretrained model (EfficientNet_B0), freeze its weights, re-define the classifier layer, fine-tune it to our problem and compare the difference.

# EfficientNet architecture after being frozen

![model](https://github.com/Haytam258/CustomDatasetWithEfficientNet/blob/main/results/EfficientNet%20Structure.png)

# Results
TinyVGG without Data Augmentation : Training Accuracy ~48%   |   Testing Accuracy ~27%  (pretty low)

TinyVGG with Data Augmentation : Training Accuracy ~42%   |   Testing Accuracy ~32%  (still low, but it's slightly better)

EfficientNet_B0 with it's original training data transformations : Training Accuracy ~79%   |   Testing Accuracy ~88% (a far better result)

# TinyVGG with data augment :
![tiny_vgg](https://github.com/Haytam258/CustomDatasetWithEfficientNet/blob/main/results/TinyVGG%20Customdataset%20with%20data%20augment.png)



# TinyVGG without data augment :
![tiny_vgg_without](https://github.com/Haytam258/CustomDatasetWithEfficientNet/blob/main/results/TinyVGG%20Customdataset%20without%20data%20augment.png)

# EfficientNet :
![efficient_net](https://github.com/Haytam258/CustomDatasetWithEfficientNet/blob/main/results/EfficientNet%20Results.png)
