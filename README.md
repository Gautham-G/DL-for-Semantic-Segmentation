# Semantic Segmentation with Deep Learning

**Overview** : This project mainly consists of two parts. They are semantic segmentation using a module named PSPNet (Pyramid Scene Parsing Network), which is implemented from scratch (original paper [here](https://arxiv.org/pdf/1612.01105.pdf)), and then using this transfer learning to apply this model to a different dataset.

**Results** : The results are seen in DL For SS.pdf

### Part A

This involves creating the PSP net, which is motivated from the original paper [here](https://arxiv.org/pdf/1612.01105.pdf). The network uses ResNet as a backbone. 

The idea is to use _dilation_ (which increases the receptive power of the network. [This](https://theaisummer.com/receptive-field/) is a good definition of receptive power, which in essence means that the network is able to increase the amount of information absorbed) and then aggregates context over different portions of the image using the 'Pyramid Pooling Module' (PPM).

The architecture is defined as below.  
![PSPNet Working](PSPNet.png?raw=true "PSPNet Working")

The data used here is from the Camvid dataset (a small set of 701 images for self-driving perception). More can be read about it [here](http://mi.eng.cam.ac.uk/research/projects/VideoRec/CamVid/) and [here] (http://www0.cs.ucl.ac.uk/staff/G.Brostow/papers/Brostow_2009-PRL.pdf).
