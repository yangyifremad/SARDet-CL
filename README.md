# SARDet-CL: Self-Supervised Contrastive Learning with Feature Enhancement and Imaging Mechanism Constraints for SAR Target Detection

This project aims to improve the performance of SAR target detection tasks by introducing a self-supervised pre-trained model SARDet-CL.In this repository, we provide the detection code built for this project and a pre-trained backbone for Gaofen-3 satellite data to the community. The self-supervised pre-trained model can be easily obtained, fine-tuned and tested on a range of other downstream tasks.
## Pretrained models
We provide a pre-trained ResNet50 backbone network trained by SARDet-CL for comparison and testing in subsequent research.

[SARDet-CL](https://pan.baidu.com/s/1TsAuIyOthmuhpSp2g1CjLg?pwd=fp91)
## Datas
[ZKXT](https://github.com/xiayang-xiao/Dataset-zkxt)

Other datasets can be obtained from Ref.

## Install
The detector is based on the MMrotate and MMdetection frameworks. For installation instructions, please refer to:

[MMrotate](https://github.com/open-mmlab/mmrotate)

[MMdetection](https://github.com/open-mmlab/mmdetection)

## Fine-tuning
You can use the following three methods to load a pre-trained model.Due to differences in framework versions, please check the logs to make sure the model is loaded correctly.
```python
1. model.backbone.pretrained = SARDet-CL.pth
2. load_from = SARDet-CL.pth
3. model.backbone.init_cfg.checkpoint = SARDet-CL.pth
```

## Test
You can use the following command to infer the dataset.

```python
python tools/test.py ${ori_rcnn_config.py} ${CHECKPOINT_FILE_by_Fine-tuning} [optional arguments]
```
