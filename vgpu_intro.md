# vGPU图形加速

EPC计算节点以UCloud快杰裸金属云主机为底座。其CPU基于2019年推出的AMD EPYC2系列，具有极高性价比。虚拟化架构为“裸金属架构”，基于NVIDIA最新系列 BlueField DPU打造，有效提升宿主机CPU性能稳定性，让快杰裸金属云主机在具备快杰云主机弹性灵活高性能诸多特性的同时，做到了物理机级别的资源隔离。

EPC计算节点支持的vGPU型号如下：
* 计算能力支持NVIDIA Tesla T4的1/4
* GPU显存支持4 GB
* [AMD EPYC 7H12](https://www.amd.com/zh-hans/products/cpu/amd-epyc-7h12)（基础主频2.6GHz，全核最大主频3.3GHz）

vGPU型实例需要使用GRID驱动，获取方式和实例的镜像类型有关：
* Windows：创建实例时在镜像市场中搜索关键词GRID，并选用预装GRID驱动的镜像。这些收费镜像带有已经激活License的GRID驱动，不用再手动安装GRID驱动。
* Linux：请自行向NVIDIA购买GRID License，并在创建实例后手动安装GRID驱动和激活License。

EPC计算节点支持的规格如下：

| CPU（核） | 内存（GB） | 系统盘（GB） |
|-----|-----|-----------|
| 32 | 64 | 200 |
| 32 | 128 | 200 |
| 64 | 128 | 200 |
| 64 | 256 | 200 |
| 96 | 192 | 200 |
| 128 | 256 | 200 |
| 240 | 480 | 200 |  
