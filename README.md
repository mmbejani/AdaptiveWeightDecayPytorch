# Adaptive Weight-Decay with Pytorch
Adaptive Weight Decay Regularization based on Pytorch Framework

# How To Use
Create an object from `AdaptiveWeightDecay`, for example:
```
model = AdaptiveWeightDecay(...)
```
To create an object set the inputs as:
1. The network that you want to train (`VGG()`).
2. The module of loss function (`nn.MSELoss()`).
3. The optimizer (`torch.optim.Adam`).
4. The increasing factor of the coefficient of weight decay.
5. The decreasing factor of the coefficient of weight decay.
6. The overfitting treshold.
7. The underfitting treshold.

After creating an object, you have to call `fit` function to train on the dataset.
```
model.fit(train_loader, test_loader, max_epoch)
```

# Requirements

To run this scheme, you need to install `numpy`, `pytorch`, and `tqdm`.

You can find more details about the scheme in [Paper](https://ieeexplore.ieee.org/abstract/document/8643569)
