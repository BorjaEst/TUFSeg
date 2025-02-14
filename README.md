# Thermal Urban Feature Segmentation (TUFSeg)

This repository contains scripts for the semantic segmentation of thermal urban features 
using the [segmentation\_models toolbox](https://github.com/qubvel/segmentation_models). 
The popular U-Net is used as the base and retrained on differently processed RGBT datasets with 
masks generated from json annotation files.

## Installation

To install all required packages, run:
```
pip3 install -r requirements.txt
``` 
The code works with Python `v3.8` and Python `v3.10`. Tensorflow and keras `v2.10` are used for 
training.

>**NOTE**:
>The [Perun](https://github.com/Helmholtz-AI-Energy/perun) package is used for energy 
> monitoring. However, for it to work properly in combination with module calls, [this forked 
> and adapted repository](https://github.com/emvollmer/perun.git) is installed instead.

## Repository structure

```
.
├── scripts
│   ├── registration    ---> optional scripts for merging raw RGB and thermal imagery into RGBTs
│   ├── setup           ---> required scripts for RGBT processing for model training
│   ├── segm_models     ---> required scripts for training, evaluating, and inferring with segmentation model(s)
│   ├── __init__.py
│   └── configuration.py    ---> configuration used across setup and segm_models
├── resources
│   ├── alignment       ---> resources used in raw image registration for alignment
│   └── calibration     ---> resources used in raw image registration for camera calibration
├── README.md
├── setup.py            ---> script for setting up the repo as a package
├── requirements.txt    ---> requirements file for installation
└── __init__.py
```

## License

This project is released under the [BSD-3-Clause license](https://github.com/emvollmer/TUFSeg/blob/main/LICENSE).

## Acknowledgement

The authors acknowledge support by the state of Baden-Württemberg through bwHPC. This work is funded by European Union through the AI4EOSC project (Horizon Europe) under Grant number 101058593.
We thank Marinus Vogl and the Air Bavarian GmbH for their support with equipment and service for the recording of images.
