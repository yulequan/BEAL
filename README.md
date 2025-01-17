# pytorch-BEAL

Code for paper 'Boundary and Entropy-driven Adversarial
Learning for Fundus Image Segmentation' early accepted by MICCAI 2019.

### Introduction
This is a PyTorch(1.0.1.post2) implementation of [BEAL](https://github.com/EmmaW8/BEAL). 
The code was tested with Anaconda and Python 3.7.1.
```Shell
    conda install pytorch torchvision cudatoolkit=9.0 -c pytorch
```

### Installation

After installing the dependency:    
``` Shell
    pip install pyyaml
    pip install pytz
    pip install tensorboardX==1.4 matplotlib pillow 
    pip install tqdm
    conda install scipy==1.1.0
    conda install -c conda-forge opencv
```

0. Clone the repo:
    ```Shell
    git clone https://github.com/EmmaW8/BEAL.git
    cd BEAL
    ```

1. Install dependencies:

    For PyTorch dependency, see [pytorch.org](https://pytorch.org/) for more details.

    For custom dependencies:
    ```Shell
    
    ```

2. Configure your dataset path in [train.py](https://github.com/EmmaW8/BEAL/blob/master/train.py) with parameter '--data-dir'.

3. You can train deeplab v3+ using mobilenetv2 or others as backbone.

    To train it, please do:
    ```Shell
    python train.py -g 0 --data-dir /data/ssd/public/sjwang/fundus_data/domain_adaptation --batch-size 8 --datasetT RIM-ONE_r3
    ```
    To test it, please do:
    Download the weights can put them into the log folder from [link](https://drive.google.com/open?id=1ZPLX937VT31KOZLtIOZjc2IBpnZIYawU).
    ```Shell
    python test.py --model-file ./logs/DGS_weights.tar --dataset Drishti-GS
    ```


