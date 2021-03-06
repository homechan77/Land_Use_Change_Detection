> #### ***quoted by https://github.com/I-Hope-Peace/DSMSCN***
 - ##### ***해당 깃허브에 공개된 논문 소스코드를 인용하였으며 지도학습 모델 가운데 하나인 FCSD(FC-Siam-Diff) 알고리즘을 활용하였다***
 - ##### ***학습 모델(train_Unet_model) 파일 실행 과정 중 발생하는 오류를 수정하였다.***
 - ##### ***기존 샘플 데이터셋 이외의 추가적인 데이터셋을 생성하여 알고리즘 모델에 적용 후 변화 탐지 결과를 예측해 보았다.***
 - ##### ***모델이 학습을 하며 생성한 가중치 값들을 기존 알고리즘 모델과 결합하여 새로운 데이터셋을 투입했을 시에 어느 정도 예측 성능을 발휘하는지 연구해 보았다.***
 - ##### ***연구 대상 데이터셋 지역은 제주도로 선정하였으며 2011년과 2019년 사이의 변화를 탐지해 보았다. 데이터는 국토지리정보원에서 제공하는 정사영상과 연속수치지형도를 활용하였다.***
 - ##### ***+추가) 국토 이용 변화 이전과 이후의 각각의 영상 사진들에 대해 unet 모델에 기반한 segmentation을 진행하고 segmentation된 결과물들을 opencv를 활용하여 차영상을 생성한다.***
 - ##### ***+추가) FCSD 알고리즘과 unet 알고리즘 모델을 활용한 국토 이용변화 결과를 비교한다.***
<div align=left><img src="./unet/unet_treestructure.jpg" width="100%" height="100%"> </div>


<br>

# DSMSCN

Tensorflow implementation for [Change Detection in Multi-temporal VHR Images Based on Deep Siamese Multi-scale Convolutional Neural Networks.](https://arxiv.org/abs/1906.11479)

<div align=center><img src="./DSMSCN-master/DSMSCN-master/Fig/DSMSCN.png" width="25.8%" height="25.8%">      <img src="./DSMSCN-master/DSMSCN-master/Fig/DSMSFCN.png" width="50%" height="50%"></div><p align="center">Left: DSMS-CN, right: DSMS-FCN</p>



## Abstract
Very-high-resolution (VHR) images can provide abundant ground details and spatial geometric information. Change detection in multi-temporal VHR images plays a significant role in urban expansion and area internal change analysis. Nevertheless, traditional change detection methods can neither take full advantage of spatial context information nor cope with the complex internal heterogeneity of VHR images. In this paper, a powerful feature extraction model entitled multi-scale feature convolution unit (MFCU) is adopted for change detection in multi-temporal VHR images. MFCU can extract multi-scale spatial-spectral features in the same layer. Based on the unit two novel deep siamese convolutional neural networks, called as deep siamese multi-scale convolutional network (DSMS-CN) and deep siamese multi-scale fully convolutional network (DSMS-FCN), are designed for unsupervised and supervised change detection, respectively. For unsupervised change detection, an automatic pre-classification is implemented to obtain reliable training samples, then DSMS-CN fits the statistical distribution of changed and unchanged areas from selected training samples through MFCU modules and deep siamese architecture. For supervised change detection, the end-to-end deep fully convolutional network DSMS-FCN is trained in any size of multi-temporal VHR images, and directly outputs the binary change map. In addition, for the purpose of solving the inaccurate localization problem, the fully connected conditional random field (FC-CRF) is combined with DSMS-FCN to refine the results. The experimental results with challenging data sets confirm that the two proposed architectures perform better than the state-of-the-art methods.

## Unsupervised Architecture
<div align=center><img src="./DSMSCN-master/DSMSCN-master/Fig/unsupervised.png" width="70%" height="70%"> </div>


## Supervised Architecture
<div align=center><img src="./DSMSCN-master/DSMSCN-master/Fig/supervised.png" width="80%" height="80%"> </div>


## Requirements
```
tensorflow_gpu==1.9.0
keras==2.2.0
opencv==3.1.1
numpy==1.19.1
```

## Citation
Please cite our paper if you use this code in your research.
```
@inproceedings{Chen2019,
author = {Chen, Hongruixuan and Wu, Chen and Du, Bo and Zhang, Liangpei},
booktitle = {2019 10th International Workshop on the Analysis of Multitemporal Remote Sensing Images, MultiTemp 2019},
doi = {10.1109/Multi-Temp.2019.8866947},
eprint = {1906.11479},
isbn = {9781728146157},
pages = {1--4},
title = {{Deep Siamese Multi-scale Convolutional Network for Change Detection in Multi-Temporal VHR Images}},
year = {2019}
}

@article{chen2020change,
title={Change Detection in Multi-temporal VHR Images Based on Deep Siamese Multi-scale Convolutional Networks}, 
author={Hongruixuan Chen and Chen Wu and Bo Du and Liangpei Zhang},
year={2020},
Journal = {arXiv preprint arXiv:1906.11479v2},
}
```

## Q & A
**For any questions, please [contact us.](mailto:Qschrx@gmail.com)**
