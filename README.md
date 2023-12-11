# LSFB: A Low-cost and Scalable Framework to Build Large-Scale Localization Benchmark for Augmented Reality
Nowadays the application of AR is expanding from small or medium environments to large-scale environments, where the visual-based localization in the large-scale environments becomes a critical demand. Current visual-based localization techniques face robustness challenges in complex large-scale environments, requiring tremendous number of data with groundtruth localization for algorithm benchmarking or model training. The previous groundtruth solutions can only be used outdoors, or require high equipment/labor costs, so they cannot be scalable to large environments for both indoors and outdoors, nor can they produce large amounts of data at a feasible cost. In this work, we propose LSFB, a novel low-cost and scalable framework to build localization benchmark in large-scale indoor and outdoor environments. The key is to reconstruct an accurate HD map of the environment. For each visual-inertial sequence captured in the environment, the groundtruth poses are obtained by joint optimization taking both the HD map and visual-inertial constraints. The experiments demonstrate the obtained groundtruth poses have cm-level accuracy. We use the proposed method to collect a localization dataset by mobile phones and AR glasses in various environments with various motions, and release the dataset as the first large-scale localization benchmark for AR.

# Video
https://github.com/zju3dv/LSFB/assets/16128141/d5848f5c-5d9a-4d8b-8f90-3a4a71c9bd58

# Our Dataset
The format of files are as follow:
Android phone /iPhone
```shell
A0/android
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
| 文件名\列号      | 1                  | 2                  | 3                | 4    | 5          | 6          | 7          | 8        | 9    | 10         |
| ---------------- | ------------------ | ------------------ | ---------------- | ---- | ---------- | ---------- | ---------- | -------- | ---- | ---------- |
| camera/data.csv  | t[s:double]   | filename[string]        |                  |      |            |            |            |          |      |            |
| imu/data.csv     | t[s:double]  | w.x[rad/s:double]   |  w.y[rad/s:double]  |   w.z[rad/s:double]     | a.x[m/s^2:double]   |   a.y[m/s^2:double]   |   a.z[m/s^2:double]   |      |            |
| attitude/data.csv  | t[s:double]  | g.x[m/s^2:double]   |  g.y[m/s^2:double] | g.z[m/s^2:double]     |    rv.x[double]        |   rv.y[double]         |     rv.z[double]       |  rv.w[double]        |      |            |
| gravity.csv      | 系统时间戳（纳秒） | x                  | y                | z    |            |            |            |          |      |            |
| rv.csv           | 系统时间戳（纳秒） | x                  | y                | z    | w          | 精确度     |            |          |      |            |
| exposureTime.csv | 系统时间戳（纳秒） | 曝光时间（纳秒）   |                  |      |            |            |            |          |      |            |
| gyr.csv          | 系统时间戳（纳秒） | x                  | y                | z    |            |            |            |          |      |            |
| acc.csv          | 系统时间戳（纳秒） | x                  | y                | z    |            |            |            |          |      |            |
| bluetooth.csv    | 时刻               | 系统时间戳（纳秒） | 设备名称（null） | uuid | major      | minor      | （null）   | （null） | rssi | 1970时间戳 |
| mf.csv           | 系统时间戳（纳秒） | x                  | y                | z    | 精确度     |            |            |          |      |            |
| gps.csv          | 系统时间戳（纳秒） | 经度               | 纬度             | 高度 | 水平精确度 | 竖直精确度 | 1970时间戳 |          |      |            |
| rtk.csv          | 详见文件首行       |                    |                  |      |            |            |            |          |      |            |

AR glasses
```shell
A0/glass
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
| 文件名\列号      | 1                  | 2                  | 3                | 4    | 5          | 6          | 7          |
| ---------------- | ------------------ | ------------------ | ---------------- | ---- | ---------- | ---------- | ---------- | 
| cam0/data.csv  | t[s:double]   | filename[string]        |                  |      |            |            |            |        
| imu/data.csv     | t[s:double]  | w.x[rad/s:double]   |  w.y[rad/s:double]  |   w.z[rad/s:double]     | a.x[m/s^2:double]   |   a.y[m/s^2:double]   |   a.z[m/s^2:double]   |    

```shell
groundturth
|--groundturth
|   |--data.csv
```

| 文件名\列号      | 1                  | 2                  | 3                | 4    | 5          | 6          | 7          | 8        | 9    | 10         |
| ---------------- | ------------------ | ------------------ | ---------------- | ---- | ---------- | ---------- | ---------- | -------- | ---- | ---------- |
|data.csv|timestamp[ns]| p_RS_R_x [m]| p_RS_R_y [m]| p_RS_R_z [m]|q_RS_w []| q_RS_x []| q_RS_y []| q_RS_z []| v_RS_R_x [m s^-1]| v_RS_R_y [m s^-1]| v_RS_R_z [m s^-1]| b_w_RS_S_x [rad s^-1]| b_w_RS_S_y [rad s^-1]| b_w_RS_S_z [rad s^-1]| b_a_RS_S_x [m s^-2]| b_a_RS_S_y [m s^-2]| b_a_RS_S_z [m s^-2]|





You can download our dataset from following addresses:

- atrium  : https://pan.baidu.com/s/1mCGWbO-LXQvozcjTdKl4zg  password: v748      
- exhibition-hall  : https://pan.baidu.com/s/1FXw5BqR4246g9CYGnK9Org  password: k4nb       
- office-park-indoor-outdoor  : https://pan.baidu.com/s/1hS4Ta5YuNepJ8DnBrQ3_Tg  password: 78ap
- corridor-narrow  : https://pan.baidu.com/s/1HsvfVNdGINg9rhheys4Z6g  password: ummv
- corridor-wide   : https://pan.baidu.com/s/1huWTLukIlrQeObgmxxzFYw  password: qq2p
- large-indoor-office : https://pan.baidu.com/s/1rC_aKvDF3K7Y1BmbFWx8WQ  password: 44ff     
- office-park-outdoor  : https://pan.baidu.com/s/1sjDc081bZBeDqD1wWQBwXA  password: nlbg
- medium-indoor-office   : https://pan.baidu.com/s/1RRFVZq-NaiTG-xWHewqgYg  password: w266 
- stairs  : https://pan.baidu.com/s/1S-_3m2GadHXreL7BwbUXIQ  password: ib9e

- Ground Truth: https://pan.baidu.com/s/1tXbO1_trKOlVLHGiCCabwA  password: l36c


# Citation

If you find this dataset useful for your research, please use the following BibTeX entry.

```bibtex
@ARTICLE{10223237,
  author={Liu, Haomin and Zhao, Linsheng and Peng, Zhen and Xie, Weijian and Jiang, Mingxuan and Zha, Hongbin and Bao, Hujun and Zhang, Guofeng},
  journal={IEEE Transactions on Circuits and Systems for Video Technology}, 
  title={A Low-cost and Scalable Framework to Build Large-Scale Localization Benchmark for Augmented Reality}, 
  year={2023},
  volume={},
  number={},
  pages={1-1},
  doi={10.1109/TCSVT.2023.3306160}}
```
