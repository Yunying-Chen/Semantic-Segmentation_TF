# Semantic-Segmentation_TF
Using Tensorflow to implement semantic segmentation

## Overview                      
In this project, the pixels of a road will be labelled in images using a Fully Convolutional Network (FCN) with [Kitti Road dataset](http://www.cvlibs.net/datasets/kitti/eval_road.php)                                  

## Dependencies                            
* Python 3                     
* Tensorflow                          
* NumPy                       
* SciPy

##  Approach                  
### Network
The fully convolutional network is based on a pre-trained [VGG-16 network](https://s3-us-west-1.amazonaws.com/udacity-selfdrivingcar/vgg.zip). With the 1x1 convolution, upsampling and adding of layer 3, layer 4 and layer 7, the VGG-16 network is converted to a fully convolutional network. The following is the graphic demonstration of the network:                                                        
![network](https://github.com/Yunying-Chen/Semantic-Segmentation_TF/blob/master/img/network.png)                                                                                       


### Hyperparameters
* keep_prob: 0.5                           
* learning_rate: 0.0001                                   
* epochs: 25                              
* batch_size: 5                               


### Run the code.
1. Clone this repo
2. Mkdir data
3. Download the [Kitti Road dataset](http://www.cvlibs.net/datasets/kitti/eval_road.php)  and place it under './data/'              
4. Run 'python main.py'
(If your code cannot download VGG-16 pre-trained model, you can download [here](https://s3-us-west-1.amazonaws.com/udacity-selfdrivingcar/vgg.zip), then unzip and place it under './data/vgg'. More detail is in helper.py)                 

## Performance
Below are a few sample images from the output of the fully convolutional network, with the segmentation class overlaid upon the original image in green.(More results can be seen in img folder)
![um_000013.png](https://github.com/Yunying-Chen/Semantic-Segmentation_TF/blob/master/img/um_000013.png)                    
![uu_000035.png](https://github.com/Yunying-Chen/Semantic-Segmentation_TF/blob/master/img/uu_000035.png)                       
![um_000015.png](https://github.com/Yunying-Chen/Semantic-Segmentation_TF/blob/master/img/um_000015.png)                      

