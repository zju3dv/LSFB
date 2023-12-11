# LSFB: A Low-cost and Scalable Framework to Build Large-Scale Localization Benchmark for Augmented Reality
Nowadays the application of AR is expanding from small or medium environments to large-scale environments, where the visual-based localization in the large-scale environments becomes a critical demand. Current visual-based localization techniques face robustness challenges in complex large-scale environments, requiring tremendous number of data with groundtruth localization for algorithm benchmarking or model training. The previous groundtruth solutions can only be used outdoors, or require high equipment/labor costs, so they cannot be scalable to large environments for both indoors and outdoors, nor can they produce large amounts of data at a feasible cost. In this work, we propose LSFB, a novel low-cost and scalable framework to build localization benchmark in large-scale indoor and outdoor environments. The key is to reconstruct an accurate HD map of the environment. For each visual-inertial sequence captured in the environment, the groundtruth poses are obtained by joint optimization taking both the HD map and visual-inertial constraints. The experiments demonstrate the obtained groundtruth poses have cm-level accuracy. We use the proposed method to collect a localization dataset by mobile phones and AR glasses in various environments with various motions, and release the dataset as the first large-scale localization benchmark for AR.


# Our Dataset

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

If you find this code useful for your research, please use the following BibTeX entry.

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
