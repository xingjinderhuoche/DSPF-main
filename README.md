# DSPF-main

# Installation
Python >= 3.7
CUDA 11.7
Pytorch >= 1.12
open3d==0.17.0
transforms3d
pytorch3d
pyyaml
opencv-python
tensorboardX
tqdm
timm==0.9.12
scipy

# Install the C++ extension module
sh install.sh

# preparing the data
1、 PCN dataset from https://drive.usercontent.google.com/download?id=1OvvRyx02-C_DkzYiJ5stpin0mnXydHQ7&amp;export=download

2、 ModelNet dataset from https://github.com/azuki-miho/OptDE

3、 3D-EPN dataset from https://github.com/CuiRuikai/Partial2Complete?tab=readme-ov-file#installation

4、 ScanNet & MatterPort3D from https://github.com/azuki-miho/OptDE

# pre-training
python pre_train.py --sourcedata your_source_dataset_path --category [chair, table, ...]

# Domain adaptation for synthetic datasets
prthon adaptation.py --sourcemodel your_pretrained_model_path --targetdatasets your_target_dataset_name --targetdata your_target_dataset_path --category [chair, table, ...]

# Domain adaptation for real-world datasets
prthon adaptation_real.py --sourcemodel your_pretrained_model_path --targetdatasets your_target_dataset_name --targetdata your_target_dataset_path --category [chair,table]
