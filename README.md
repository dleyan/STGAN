# Graph Convolutional Adversarial Networks for Spatio-Temporal Anomaly Detection

Two datasets are available at [Google Drive](https://drive.google.com/drive/folders/1U4ehoLEV83JLpPIXbopng0ydwfOAFLqN?usp=share_link).
**If you use the data, please cite the following paper.**
```
@ARTICLE{9669110,
  author={Deng, Leyan and Lian, Defu and Huang, Zhenya and Chen, Enhong},
  journal={IEEE Transactions on Neural Networks and Learning Systems}, 
  title={Graph Convolutional Adversarial Networks for Spatiotemporal Anomaly Detection}, 
  year={2022},
  volume={},
  number={},
  pages={1-13},
  doi={10.1109/TNNLS.2021.3136171}}
```
**PeMS dataset (bay)** is collected from [PeMS](https://pems.dot.ca.gov/) and **NYC dataset (nyc)** is provided by [Detecting Collective Anomalies from Multiple Spatio- Temporal Datasets across Different Domains](https://www.microsoft.com/en-us/research/publication/detecting-collective-anomalies-from-multiple-spatio-temporal-datasets-across-different-domains/). 
Each dataset consists of the following five datasets:
+ data.npy
+ node_subgraph.npy
+ node_adjacent.txt
+ time_features.txt
+ node_dist.txt

where the `data.npy` is the traffic data in Bay area or New York City; 
`node_subgraph.npy` represents the adjacency matrix of the subgraph of each node; 
`node_adjacent.txt` represents all nodes in the subgraph of each node;  `time_features.txt` represents the time feature of each time slots; 
`node_dist.txt` represents the distance between nodes.

We also provide the information of the selected sensors in our paper, the file is `vds_info.csv`. 

------------------------------------------------------
We have updated the ground truth of PeMS datasets. Note that we didn't delete the CHP incidents with duration<=0 since we extended the end time of each incident by 1 hour to include the impact of the traffic accidents. The ground truth of NYC dataset is provided by the authors of paper [Detecting Collective Anomalies from Multiple Spatio-Temporal Datasets across Different Domains](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/02/Collective20anomalies-GIS2015_yu.pdf).

If you need anomaly labels for other times, please refer to [CHP incident](https://pems.dot.ca.gov/?dnode=State&content=incidents&tab=inc_detail) and [LCS Report](https://pems.dot.ca.gov/?q=cnt&s_time_id=1658620800&e_time_id=1666655940&lcs_date_type=0&lcs_filter_mode=show_adv&gn=week&html_x=42&report_form=1&facility%5B%5D=HOV&dnode=State&content=lcs&tab=lcs_list). I hope they will be helpful to you.

> If you have any question about the code or the paper, please contact me by email (dleyan@mail.ustc.edu.cn). 
