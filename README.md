# HoHoNet

This is the implementation of our CVPR'21 "[HoHoNet: 360 Indoor Holistic Understanding with Latent Horizontal Features
](https://arxiv.org/abs/2011.11498)".


## Dataset
Detail instruction for preparing the datas for each dataset and task:
- `Matterport3d` x `Layout`: **TODO**
- `Matterport3d` x `Depth (BiFuse's stitched)`: **TODO**
- `Matterport3d` x `Depth (our new stitched)`: **TODO**
- `Stanford2d3d` x `Depth`: **TODO**
- `Stanford2d3d` x `Semantic segmentation`: **TODO**

The overall file strucure of the datasets is depicted as follow:

    data
    ├── mp3d_align                 # Stitching provided by BiFuse (https://github.com/Yeh-yu-hsuan/BiFuse)
    │   ├── 17DRP5sb8fy
    │   │   ├── 00ebbf3782c64d74aaf7dd39cd561175
    │   │   │   ├── color.jpg
    │   │   │   └── depth.npy
    │   │   └── ...
    │   └── ...
    │
    ├── matterport3d
    │   ├── scenes_abla_train.txt  # 41 house id for ablation training
    │   ├── scenes_abla_valid.txt  # 20 house id for ablation evaluation
    │   ├── scenes_train.txt       # 61 house id for training following BiFuse
    │   ├── mp3d_scenes_test.txt   # 28 house id for testing following BiFuse
    │   └── mp3d_rgbd/             # Our new stitching which fixs the depth noise in BiFuse's version
    │                              # Release new stitching code with new experiments later.
    │
    ├── mp3d_layout                # Please follow README_prepare_data_mp3d_layout.md
    │   ├── train
    │   │   ├── img/*png
    │   │   └── label_cor/*txt
    │   ├── valid
    │   │   ├── img/*png
    │   │   └── label_cor/*txt
    │   └── test
    │       ├── img/*png
    │       └── label_cor/*txt
    │
    ├── stanford2D3D               # Please follow README_prepare_data_s2d3d_depth.md
    │   ├── area_[1|2|3|4|5a|5b|6]
    │   │   ├── img/*png
    │   │   └── depth/*png
    │   ├── small_[train|valid|test].txt
    │   └── fold[1|2|3]_[train|valid].txt
    │
    └── s2d3d_sem                  # Please follow README_prepare_data_s2d3d_sem.md
        └── area_[1|2|3|4|5a|5b|6]
            ├── rgb/*png
            └── semantic/*png
