# Classifying point clouds at the facade-level using geometric features and deep learning networks

## Description
This project mainly focus on classifying point clouds of TUM buildings. Basically, there are 3 kinds of models that used in this project: Random Forest, PointNet, PointNet++. Except xyz coordinates, geometric features are also taken as input data.
By comparing classification results with and without geometric features, we can see how the geometry features improve the performance of networks.

[RF_xyz.ipynb](RF_xyz.ipynb) is for the model Random Forest with large dataset and only xyz coordiantes as the input data.

[RF_xyz_sd.ipynb](RF_xyz_sd.ipynb) is for the model Random Forest with small dataset and only xyz coordiantes as the input data.

[RF_xyz_xyzpoc.ipynb](RF_xyz_xyzpoc.ipynb) is for the model Random Forest with small dataset and both xyz coordiantes and geometric features as the input data. In this code, the importance for all the geometric features is calculated

[PointNet_xyz_v2.ipynb](PointNet_xyz_v2.ipynb) is for the model PointNet, which is part of the PointNet++. The input data is xyz coordinates only.

[PointNet_xyzpoc_v2.ipynb](PointNet_xyzpoc_v2.ipynb) is also for the model PointNet. The input data includes geometric features. All the test for PointNet is based on small dataset.

[PointNet2_xyz.ipynb](PointNet2_xyz.ipynb) is for the model PointNet++ based on large dataset. The input data is xyz coordinates only.

[PointNet2_xyz_sd.ipynb](PointNet2_xyz_sd.ipynb) is also for the PointNet++ based on small dataset. The input data is xyz coordinates only.

[PointNet2_xyznpoc_colab.ipynb](PointNet2_xyznpoc_colab.ipynb) is also for the PointNet++, and this version is for Google Colab. The input data is xyz coordinates and geometric features as well.

## Visuals
Visualization for small dataset and large dataset:

| Dataset | Training Data | Test Data |
|--|--|--|
| Small |![](/re_pic/Training_sd.png)| ![](/re_pic/Test_sd.png)|
| Large |![](/re_pic/Training_Ld.png)| ![](/re_pic/Test_ld.png)|

## Classification

### Performance
| Model | Small Dataset<br>(xyz only) | Large Dataset<br>(xyz only) | Small Dataset<br>(xyz&9 geometric features) | Small Dataset<br>(xyz&6 geometric features) | Large Dataset<br>(xyz&9 geometric features) | Large Dataset<br>(xyz&6 geometric features) |
|--|--|--|--|--|--|--|
| Random Forest |  33.2%| 68.4% | 49.7% | 49.1 | 66.5% | 64.2%|
| PointNet | 39.6% | 69.1% | 55.8% | 52.1% | 78.5% | 85.5% |
| PointNet++ |  54.8% | 83.1% | 39.2% | **62.1%** | 84.7% | **87.5%** |

## Reference by
[yanx27/Pointnet_Pointnet2_pytorch](https://github.com/yanx27/Pointnet_Pointnet2_pytorch)<br>
