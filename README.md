# Semantic Image Segmentation - DeepLab v3

Our implementation of the DeepLabv3 is entirely based on the paper ["Rethinking Atrous Convolution for Semantic Image Segmentation"](https://arxiv.org/abs/1706.05587). 
This paper tackles with two main problems in semantic image segmentation. 

1) Consecutive pooling operations and convolution striding are necessary for DCNNs to learn increasingly abstract feature representations. However, they cause reduced feature resolution which may impede dense prediction tasks, where detailed spatial information is desired.  Chen et al's proposed approach is to use atrous convolution, a.k.a dilated convolution, to repurpose ImageNet pretrained networks to extract denser feature maps by removing the downsam- pling operations from the last few layers and upsampling the corresponding filter kernels, equivalent to inserting holes between filter weights.

2) The existence of objects at multiple scales is the second important challenge in semantic segmentation. Different DNN architectures have been developed to capture multi-scale context, such as image pyramid, encoder-eecoder, deeper with atrous convolution, spatial pyramid pooling. They chose to implement the [Atrous Spatial Pyramid Pooling (ASPP) method](https://arxiv.org/abs/1606.00915). 

In the end, their proposed model, ‘DeepLabv3’ improves over their previous works [DeepLabv2](https://arxiv.org/abs/1606.00915), [DeepLabv1](https://arxiv.org/abs/1412.7062) and attains performance of 85.7% on the PASCAL VOC 2012 test set without DenseCRF post- processing." 
