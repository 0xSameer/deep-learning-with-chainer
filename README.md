# Deep Learning with Chainer  

* Deep Convolutional Neural Networks (Python 2 or 3)  
[chainer-cnn-cifar10.ipynb](https://github.com/masaki-y/deep-learning-with-chainer/blob/master/chainer-cnn-cifar10.ipynb)

* Fine-tuning Caffemodel (Python 2)  
[chainer-fine-tuning.ipynb](https://github.com/masaki-y/deep-learning-with-chainer/blob/master/chainer-fine-tuning.ipynb)

* Auto Encoder and Learned Filter Visualization (Python 2 or 3)  
[chainer-auto-encoder.ipynb](https://github.com/masaki-y/deep-learning-with-chainer/blob/master/chainer-auto-encoder.ipynb)

## Examples  
* Prediction of CNN  
![ship image in CIFAR-10](/examples/cifar10-ship.png)
```
# 1| ship         |  67.495%
# 2| automobile   |  32.491%
# 3| airplane     |   0.013%
# 4| truck        |   0.001%
# 5| frog         |   0.000%
```
* Feature maps of the 1st layer  
![feature maps](/examples/cifar10-fmap.png)

* Training CNN  
![training loss](/examples/cifar10-loss.png)  

* Prediction of fine-tuned CNN   
![buttercup image in dataset](/examples/finetuning-buttercup.png)
```
# 1| Buttercup    |  90.449%
# 2| Iris         |   7.200%
# 3| Daffodil     |   1.860%
# 4| Sunflower    |   0.279%
# 5| Tigerlily    |   0.156%
```

* Achieved filters by unsupervised learning on AE  
![Visualized Filters](/examples/ae-w-drop-relu-adam-epoch500.png)  

## Dependencies
Python 2 (or 3), [chainer](http://chainer.org/), jupyter, matplotlib, scikit-image, tqdm  

## Usage
Open a Jupyter's session in your browser.  
```shellsession
➜  jupyter notebook Chainer-CNN-CIFAR10.ipynb
```
Then select the `Run All` from the `cell` in the top menu.  

If you use a GPU, set the GPU ID to `gpuid` in the jupyter notebook.
Chainer will switch automatically to GPU mode.
```py
gpuid = -1 # gpu device ID (cpu if this negative)
xp = cuda.cupy if gpuid >= 0 else np  
```
