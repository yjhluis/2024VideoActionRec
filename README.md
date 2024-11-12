
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

## Acknowledgement



## Related linkes

- [MMDetection](https://github.com/open-mmlab/mmdetection): OpenMMLab detection toolbox and benchmark.
- [MMAction2](https://github.com/open-mmlab/mmaction2): OpenMMLab Video Action Recognition toolbox and benchmark.
