# Baselines
This is the code of *An Empirical Analysis on Multi-turn Conversational Recommender Systems.* The baselines of this paper consist of five methods: 
1. CRM; 
2. EAR;
3. SCPR;
4. CRIF;
5. UNICORE. 

## Running environment
  - numpy==1.19.1
  - pandas==1.1.1
  - scikit-learn==0.23.2    
  - scipy==1.5.2 
  - tqdm
  - matplotlib
  - torch ==1.10.0 
  - easydict==1.9  
  - regex==2021.4.4
  - torch_cluster==1.6.0
  - torch_scatter==2.0.9
  - torch_sparse==0.6.12
  - torch_spline_conv==1.2.1
  - torch_geometric
  - dgl==0.9.1

  
## Datasets
Following the majority of state-of-the art (SOTA) multi-turn CRSs, we conduct extensive experiments on two widely-used benchmark datasets, including LastFM and Yelp. In particular, LastFM is a dataset for music artists, which involves users’ music listening history, the attributes of music artists, friends of users, and users’ preferred attributes. It consists of 33 coarse-grained attributes and 8438 fine-grained attributes. Yelp contains users’ check-in records towards various businesses, the attributes (e.g., category hierarchy) of businesses, and friends of users. It features a two-layer taxonomy consisting of 29 first-layer and 590 second-layer attributes. Following the majority of multi-turn CRSs, users with fewer than 10 interactions are filtered out, and each dataset is randomly split for training, validation, and testing in a ratio of 7:1.5:1.5. Please download the datasets "data.rar" from https://drive.google.com/file/d/1r8Vp_0C5GN9oV8sQ-JQVtxBSujTZ6luQ/view?usp=sharing.

      
## How to run
To run each baseline, you can use the following command directly. Change Parsers in need. 

- CRM: cd ./EAR/lib/user-simulator, python run.py -mod crm
- EAR: cd ./EAR/lib/user-simulator, python run.py -mod ear
- SCPR: cd ./SCPR, python RL_model.py
- CRIF: cd ./CRIF, python train_agent_ear.py
- UNICORE: cd ./UNICORE, python RL_model.py


## Reference
CRM -- https://ear-conv-rec.github.io

Sun, Yueming and Zhang, Yi, Conversational Recommender System, Proceedings of the 41th International ACM SIGIR Conference on Research and
Development in Information Retrieval.

EAR -- https://ear-conv-rec.github.io            

Lei, Wenqiang and He, Xiangnan and Miao, Yisong and Wu, Qingyun and Hong, Richang and Kan, Min-Yen and Chua, Tat-Seng, Estimation-Action-Reflection: Towards Deep Interaction Between Conversational and Recommender Systems, Proceedings of the 13th International Conference on Web Search and Data Mining.

SCPR -- https://cpr-conv-rec.github.io/

Lei, Wenqiang, Zhang, Gangyi, He, Xiangnan, Miao, Yisong, Wang, Xiang, Chen, Liang, and Chua, Tat-Seng, Interactive Path Reasoning on Graph for Conversational Recommendation, Proceedings of the 26th ACM SIGKDD International Conference on Knowledge Discovery & Data Mining.

CRIF -- https://github.com/Studenthc/CRIF

Hu, Chenhao, Huang, Shuhua, Zhang, Yansen, and Liu, Yubao, Learning to Infer User Implicit Preference in Conversational Recommendation, Proceedings of the 45th International ACM SIGIR Conference on Research and Development in Information Retrieval.

UNICORE -- https://github.com/dengyang17/unicorn

Deng, Yang, Li, Yaliang, Sun, Fei, Ding, Bolin, and Lam, Wai, Unified Conversational Recommendation Policy Learning via Graph-Based Reinforcement Learning, Proceedings of the 44th International ACM SIGIR Conference on Research and Development in Information Retrieval.