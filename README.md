
# 쓰레기 무단투기 ...

## Introduction

데모 프로그램 소개

## Installation

**가상환경 생성**
```
python3.8 -m venv venv
source ./venv/bin/activate
pip install -U pip
```

#### Dependencies
- CUDA11.8
- Python3.8
- pytorch 2.0.0+cu118
- torchvision 0.15.1+cu118


**mmaction 관련 패키지 설치**
```
pip install -U openmim
mim install mmengine
mim install "mmcv==2.1.0"
mim install mmdet
```

**Project build**
```
git clone "this repository" project
cd project
pip install -v -e .
```

## Run
Video input Video output
download link (weight file) : [i3d_imagenet-pretrained-r50-heavy_8xb8-32x2x1-100e_kinetics400-rgb_trained_by_hnu_epoch_40.pth]()
download link (demo video, dump) : [i3d_imagenet-pretrained-r50-heavy_8xb8-32x2x1-100e_kinetics400-rgb_trained_by_hnu_epoch_40.pth]()
```
python demo/demo_visualize.py configs/recognition/i3d/i3d_dense_trained_by_hnu.py \
    i3d_imagenet-pretrained-r50-heavy_8xb8-32x2x1-100e_kinetics400-rgb_trained_by_hnu_epoch_40.pth \
    demo/167-3_cam02_dump02_place04_day_summer.mp4 tools/data/kinetics/label_map_hnu_label.txt \
    --out-filename output.mp4
```

| ![사진1](resources/1_night_summer.jpg) | ![사진2](resources/2_day_spring.jpg) |
|:-----------------:|:---------------:|
| 투기행위 신뢰도 : 0.78 (야간)             | 투기행위 신뢰도 : 0.98 (주간)           |
| ![사진3](resources/3_day_summer.jpg) | ![사진4](resources/4_day_summer.jpg) |
| 투기행위 신뢰도 : 0.91 (주간)             | 투기행위 신뢰도 : 0.92 (주간)           |

## Acknowledgement



## Related linkes

- [MMDetection](https://github.com/open-mmlab/mmdetection): OpenMMLab detection toolbox and benchmark.
- [MMAction2](https://github.com/open-mmlab/mmaction2): OpenMMLab Video Action Recognition toolbox and benchmark.
