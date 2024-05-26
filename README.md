# LSFB: A Low-cost and Scalable Framework to Build Large-Scale Localization Benchmark for Augmented Reality
Nowadays the application of AR is expanding from small or medium environments to large-scale environments, where the visual-based localization in the large-scale environments becomes a critical demand. Current visual-based localization techniques face robustness challenges in complex large-scale environments, requiring tremendous number of data with groundtruth localization for algorithm benchmarking or model training. The previous groundtruth solutions can only be used outdoors, or require high equipment/labor costs, so they cannot be scalable to large environments for both indoors and outdoors, nor can they produce large amounts of data at a feasible cost. In this work, we propose LSFB, a novel low-cost and scalable framework to build localization benchmark in large-scale indoor and outdoor environments. The key is to reconstruct an accurate HD map of the environment. For each visual-inertial sequence captured in the environment, the groundtruth poses are obtained by joint optimization taking both the HD map and visual-inertial constraints. The experiments demonstrate the obtained groundtruth poses have cm-level accuracy. We use the proposed method to collect a localization dataset by mobile phones and AR glasses in various environments with various motions, and release the dataset as the first large-scale localization benchmark for AR.

# Video
https://github.com/zju3dv/LSFB/assets/16128141/d5848f5c-5d9a-4d8b-8f90-3a4a71c9bd58

# Our Dataset
## Devices Info
|       | Android phone   | iPhone      | AR glasses         | 
| ---------------- | ------------------ | ------------------ | ---------------- | 
|  #Cam. | 1 | 1| 2|
|Res.|640x480|640x480|640x400|
|Fov|67x53|68x53|126x80|
|Freq.|30Hz|30Hz|30Hz|
|GS/RS*|RS|RS|GS|

\* Global shutter / rolling shutter

## Dataset Format
The format of files are as follow:

### Android phone / iPhone
```shell
eg: data/Android phone/A0/android.tar.gz
|--camera
|   |--images
|     |--17896609415000.jpg
|     |--17896643028000.jpg
|     |--...
|   |--data.csv
|   |--sensor.yaml
|--imu
|   |--data.csv
|   |--sensor.yaml
|--attitude
|   |--data.csv
|   |--sensor.yaml
|--sensor
|   |--bluetooth.csv
|   |--mf.csv
|   |--gps.csv
|   |--...

```
Data description
| File name         |  1        |  2                |  3                |  4                |  5                |  6                |  7                |
|-----------------|------------|--------------------|--------------------|--------------------|--------------------|--------------------|--------------------|
| camera/data.csv  | t[s:double]   | filename[string]        |                  |      |            |            |            |          |     
| imu/data.csv     | t[s:double]  | w.x[rad/s:double]   |  w.y[rad/s:double]  |   w.z[rad/s:double]     | a.x[m/s^2:double]   |   a.y[m/s^2:double]   |   a.z[m/s^2:double]   |     
| attitude/data.csv  | t[s:double]  | g.x[m/s^2:double]   |  g.y[m/s^2:double] | g.z[m/s^2:double]     |    rv.x[double]        |   rv.y[double]         |     rv.z[double]       |  rv.w[double]        |    

### AR glasses
```shell
eg: data/AR glasses/A0/glass.tar.gz
|--cam0
|   |--data
|     |--00000001709367764079.png
|     |--00000001709401349068.png
|     |--...
|   |--data.csv
|   |--sensor.yaml
|--cam1
|   |--data
|     |--00000001709367764079.png
|     |--00000001709401349068.png
|     |--...
|   |--data.csv
|   |--sensor.yaml
|--imu0
|   |--data.csv
|   |--sensor.yaml

```
Data description
| File name         |  1        |  2                |  3                |  4                |  5                |  6                |  7                |
|-----------------|------------|--------------------|--------------------|--------------------|--------------------|--------------------|--------------------|
| cam0/data.csv   | t[s:double]   | filename[string]        |                  |      |            |            |            |          |     
| imu/data.csv     | t[s:double]  | w.x[rad/s:double]   |  w.y[rad/s:double]  |   w.z[rad/s:double]     | a.x[m/s^2:double]   |   a.y[m/s^2:double]   |   a.z[m/s^2:double]   |     


### groundturth
```shell
eg: groundturth/Android phone/A0/
|--groundturth
|   |--data.csv
```

|File name| 1  | 2  | 3 | 4  | 5   | 6  | 7   | 8  | 9  | 10 | 11|12|13|14|15|15|17|
|-----------| -----------| -----------| ----------- | -- | -- | --| -- | -- | -- | -- |-|-|-|-|-|-|-|
|groundturth/data.csv|timestamp[ns]| p_RB_R_x [m]| p_RB_R_y [m]| p_RB_R_z [m]|q_RB_w []| q_RB_x []| q_RB_y []| q_RB_z []| v_RB_R_x [m s^-1]| v_RB_R_y [m s^-1]| v_RB_R_z [m s^-1]| b_w_RB_S_x [rad s^-1]| b_w_RB_S_y [rad s^-1]| b_w_RB_S_z [rad s^-1]| b_a_RB_S_x [m s^-2]| b_a_RB_S_y [m s^-2]| b_a_RB_S_z [m s^-2]|

### Motion and ScenrType of Sequences
Various types of environments in the dataset:
![Image](https://github.com/zju3dv/LSFB/blob/main/assets/environments.png)

Various types of motions in the dataset:
![Image](https://github.com/zju3dv/LSFB/blob/main/assets/motions.png)

# Download
You can download our dataset from following addresses:

https://pan.baidu.com/s/1W1KluP2V77j5HAQwblh0vQ?pwd=n985


# Citation

If you find this dataset useful for your research, please use the following BibTeX entry.

```bibtex
@ARTICLE{10223237,
  author={Liu, Haomin and Zhao, Linsheng and Peng, Zhen and Xie, Weijian and Jiang, Mingxuan and Zha, Hongbin and Bao, Hujun and Zhang, Guofeng},
  journal={IEEE Transactions on Circuits and Systems for Video Technology}, 
  title={A Low-cost and Scalable Framework to Build Large-Scale Localization Benchmark for Augmented Reality}, 
  year={2023},
  pages={1-1},
  doi={10.1109/TCSVT.2023.3306160}}
```

# Copyright

This work is affiliated with ZJU-SenseTime Joint Lab of 3D Vision, and its intellectual property belongs to SenseTime Group Ltd.

```
Copyright (c) ZJU-SenseTime Joint Lab of 3D Vision. All Rights Reserved.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```
