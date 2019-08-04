# CWCV2019-Amur-Tiger-Re-ID

This code is mainly for the **Tiger Re-ID in the plain track** and **Tiger Re-ID in the wild track**[CVWC2019](https://cvwc2019.github.io/challenge.html) @ICCV19 Workshop.

## Getting Started
### Clone the repo:

```
git clone https://github.com/LcenArthas/CWCV2019-Amur-Tiger-Re-ID.git
```
### Dependencies

Tested under python3.6  Ubantu16.04

- python packages
  - pytorch=1.0.1
  - torchvision==0.2.1
  - pytorch-ignite=0.1.2 (Note: V0.2.0 may result in an error)
  - yacs==0.1.6
  - tensorboardx
  - h5py==2.9.0
  - imgaug==0.2.9
  - matplotlib==3.1.0
  - numpy==1.16.4
  - opencv==4.1.0.15
  - pillow==6.0.0
  - scikit-image==0.15.0
  - scipy==1.3.0
  - tensorboardx==1.6
  - tqdm==4.32.1
  - yacs==0.1.6

## Section1  The Tiger Plain Re-ID:

### Train

**TO DO...**

### Inference

#### Data Preparation

Creat a new folder named `/reid_test/` under the `{repo_root}/data/AmurTiger/`:

```
cd data
cd AmurTiger
mkdir reid_test
```

Put the test images in the `{repo_root}/data/AmurTiger/reid_test/`.

#### Download Pretrained Model

The trained weight is following:

 - [Trained weight](https://pan.baidu.com/s/1q5Wdzcq6aKtM1H_VugCe3w)

Download it and create a new folder under the {repo_root} named `/trained_weight/`

```
mkdir trained_weight
```

Unzip the model.zip and put them into the `{repo_root}/trained_weight/`.

**And make sure the repo files as the following structure:**
  ```
  {repo_root}
  ├── config
  ├── configs
  ├── data
  |   ├── AmurTiger
  │   │   ├── flod0
  │   │   └── reid_test
  │   │       ├── 000000.jpg
  │   │       ├── 000004.jpg
  │   │       ├── 000005.jpg
  │   │       ├── 000006.jpg
  │   │       ├── 000008.jpg
  │   │       └── ...
  │   ├── datasets
  │   ├── samplers
  │   └── ...
  ├── engine
  ├── layers
  ├── modeling
  ├── solver
  ├── tests
  ├── trained_weight
  │   ├── best_model.pth
  │   │       ├── 000005.jpg
  │   │       ├── 000006.jpg
  │   │       ├── 000008.jpg
  │   └──     └── ...
  ├── utils
  ├── check_result.py
  ├── medo.py
  ├── medo_wide.py
  ├── test.py
  └── train.py
      
  ```
  
#### Inference Now!

```
python demo.py
```

This process will take about 15 minutes, just a moment, please. 

Run this scrip will generate 1 files in the {repo_root/}:

- **submission.json** — you can submit in the Tiger Plain Re-ID track (0.45988 mAP in the Public Leaderboard).


## Section2  The Tiger Wild Re-ID:

### Train

**TO DO...**

### Inference

**In this task, it's a two-step process: Detection and Re-id**

#### Detection

Please follow this repo: [CWCV2019-Amur-Tiger-Detection](https://github.com/LcenArthas/CWCV2019-Amur-Tiger-Detection)

#### Data Preparation

Creat a new folder named `/reid_test/` under the `{repo_root}/data/AmurTiger/`:

```
cd data
cd AmurTiger
mkdir reid_test
```

Put the test images in the `{repo_root}/data/AmurTiger/reid_test/`.

#### Download Pretrained Model

The trained weight is following:

 - [Trained weight](https://pan.baidu.com/s/1q5Wdzcq6aKtM1H_VugCe3w)

Download it and create a new folder under the {repo_root} named `/trained_weight/`

```
mkdir trained_weight
```

Unzip the model.zip and put them into the `{repo_root}/trained_weight/`.

**And make sure the repo files as the following structure:**
  ```
  {repo_root}
  ├── config
  ├── configs
  ├── data
  |   ├── AmurTiger
  │   │   ├── flod0
  │   │   └── reid_test
  │   │       ├── 000000.jpg
  │   │       ├── 000004.jpg
  │   │       ├── 000005.jpg
  │   │       ├── 000006.jpg
  │   │       ├── 000008.jpg
  │   │       └── ...
  │   ├── datasets
  │   ├── samplers
  │   └── ...
  ├── engine
  ├── layers
  ├── modeling
  ├── solver
  ├── tests
  ├── trained_weight
  │   ├── best_model.pth
  │   │       ├── 000005.jpg
  │   │       ├── 000006.jpg
  │   │       ├── 000008.jpg
  │   └──     └── ...
  ├── utils
  ├── check_result.py
  ├── medo.py
  ├── medo_wide.py
  ├── test.py
  └── train.py
      
  ```
  
#### Inference Now!

```
python demo.py
```

This process will take about 15 minutes, just a moment, please. 

Run this scrip will generate 1 files in the {repo_root/}:

- **submission.json** — you can submit in the Tiger Plain Re-ID track (0.45988 mAP in the Public Leaderboard).

