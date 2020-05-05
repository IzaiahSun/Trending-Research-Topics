*   题目：Secure Distributed Dynamic State Estimation in Wide-Area Smart Grids  
*   作者：Mehmet Necip Kurt, Yasin Yılmaz, Xiaodong Wang  
*   来源：IEEE Transactions on Information Forensics and Security, Volume 15  
*   链接：<https://ieeexplore.ieee.org/document/8759957>  
-----------------------------

## 1、主要内容  
智能电网是一个有着较多安全问题的大型复杂网络，从PMU到控制中心数据中心都易受网络攻击，本文提出了一种针对广域智能电网的安全分布式动态状态估计机制，该机制通过区块链保护数据库及通信信道安全，可以实时监测测量异常并消除其对状态估计过程的影响，还通过一种分布式信任管理方案实时监测行为异常的节点。  

## 2、创新点  
+   当下所有智能电网全部是中心化系统，本文以区块链为基础提出了一种分布式的存储方式，在每个节点（本地中心）中维护一个“账单”，记录电力信息状态，大大提高数据的机密性、可用性。  
+   通过非对称加密算法（SHA、ECC）保护通信信道安全  
+   以卡尔曼滤波算法为基础提出（随着时间的推移)获取并监视一个单变量汇总的统计信息以判断其是否处于异常状态的方法  

## 3、缺点  
+   智能电网是一个复杂的大型网络，节点繁多，以区块链为基础进行分布式存储可能会大大提高计算复杂度，也会存在网络拥塞、通信延迟导致的同步问题。  
+   文中仅给出了异常节点的识别但并未说明如何应对/恢复。  

## 4、改进  
+   可以考虑分层管理、分时间段存储状态信息的方式，将诸多节点根据其地域位置划分成多个节点集，在每个节点集中使用区块链分布式存储该节点集各节点的状态信息，上层再使用区块链存储各节点集的状态信息，每个节点集中需要有多个节点与上层对接以保证信息的可用性。