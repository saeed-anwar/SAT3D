# SAT3D

This repository is an official implementation of the [SAT3D: Slot Attention Transformer for 3D Point Cloud Semantic Segmentation](https://arxiv.org/).

By Muhammad Ibrahim, Naveed Akhtar, Saeed Anwar, and Ajmal Mian
## News


## Coming soon
- [ ] Segmentation code.
- [ ] Segmentation Model.
- [ ] Results


## Introduction

**InternImage**, initially described in [arxiv](https://arxiv.org/abs/2211.05778), can be a general backbone for computer vision.
It takes deformable convolution as the core operator to obtain large effective receptive fields, and introducing adaptive spatial aggregation
to reduces the strict inductive bias. Our model makes it possible to learn more stronger and robust models with large-scale parameters from massive data.

<div align=center>
<img src='./figs/arch.png' width=400>
</div>

## Main Results on ImageNet with Pretrained Models

**ImageNet-1K and ImageNet-22K Pretrained InternImage Models**

| name | pretrain | resolution |acc@1 | #params | FLOPs |
| :---: | :---: | :---: | :---: | :---: | :---: | 
| InternImage-T | ImageNet-1K | 224x224 | 83.5 | 30M | 5G |
| InternImage-S | ImageNet-1K | 224x224 | 84.2 | 50M | 8G |
| InternImage-B | ImageNet-1K | 224x224 | 84.9 | 97M | 16G |
| InternImage-L | ImageNet-22K | 384x384 | 87.7 | 223M | 108G |
| InternImage-XL | ImageNet-22K | 384x384 | 88.0 | 335M | 163G |

## Main Results on Downstream Tasks

**COCO Object Detection**

| backbone | method | lr schedule | box mAP | mask mAP | #params | FLOPs |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| InternImage-T | Mask R-CNN | 1x | 47.2 | 42.5 | 49M | 270G |
| InternImage-S | Mask R-CNN | 1x | 47.8 | 43.3 | 69M | 340G |
| InternImage-B | Mask R-CNN | 1x | 48.8 | 44.0 | 115M | 501G |
| InternImage-L | Cascade Mask R-CNN | 1x | 54.9 | 47.7 | 277M | 1399G |
| InternImage-XL | Cascade Mask R-CNN | 1x | 55.3 | 48.0 | 387M | 1782G |

**ADE20K Semantic Segmentation**

| backbone | resolution | single scale | multi scale | #params | FLOPs|
| :---: | :---: | :---: | :---: | :---: | :---: | 
| InternImage-T | 512x512 | 47.9 | 48.1 | 59M | 944G | 
| InternImage-S | 512x512 | 50.1 | 50.9 | 80M | 1017G |
| InternImage-B | 512x512 | 50.8 | 51.3 | 128M | 1185G |
| InternImage-L | 640x640 | 53.9 | 54.1 | 256M | 2526G |
| InternImage-XL | 640x640 | 55.0 | 55.3 | 368M | 3142G |

## Citation

If this work is helpful for your research, please consider citing the following BibTeX entry.

```
@article{Ibrahim2023SAT3D,
  title={SAT3D: Slot Attention Transformer for 3D Point Cloud Semantic Segmentation},
  author={Ibrahim, Muhammad and Akhtar, Naveed and Anwar, Saeed and Mian, Ajmal},
  journal={IEEE Transactions on Intelligent Transportation Systems (T-ITS)},
  year={2023}
}

@article{Ibrahim2023slice,
  title={Slice Transformer and Self-supervised Learning for 6DoF Localization in 3D Point Cloud Maps},
  author={Ibrahim, Muhammad and Akhtar, Naveed and Anwar, Saeed and Wise, Michael and Mian, Ajmal},
  journal={IEEE International Conference on Robotics and Automation (ICRA)},
  year={2023}
}
```
