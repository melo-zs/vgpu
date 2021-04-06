# vGPU图形加速

挂载vGPU的EPC产品能让您访问具有数千个计算内核的NVIDIA GPU，利用CUDA或开放计算语言(OpenCL)并行计算框架，为科学、工程和渲染应用程序加速。还可以将这些实例用于图形应用程序，包括游戏流式处理、3-D应用流式处理和其他图形工作负载。

EPC支持的vGPU型号：
* 计算能力支持NVIDIA Tesla T4的1/4
* GPU显存支持4 GB

vGPU型实例需要使用GRID驱动，获取方式和实例的镜像类型有关：
* Windows：创建实例时在下拉Windows镜像列表，并选用预装GRID驱动的镜像。这些镜像带有已经激活License的GRID驱动，不用再手动安装GRID驱动。
* Linux：请自行向[NVIDIA](https://enterpriseproductregistration.nvidia.com/?LicType=EVAL&ProductFamily=vGPU) 购买GRID License，并在创建实例后手动安装GRID驱动和激活License。

EPC计算节点支持的规格如下：

| CPU（核） | 内存（GB） | 系统盘（GB） | GPU | GPU显存（GB）|
|-----|-----|-----------|-----------|-----|
| 32 | 64 | 200 | T4*1/4 | 4 |
| 32 | 128 | 200 | T4*1/4 | 4 |
| 64 | 128 | 200 | T4*1/4 | 4 |
| 64 | 256 | 200 | T4*1/4 | 4 |
| 96 | 192 | 200 | T4*1/4 | 4 |
| 128 | 256 | 200 | T4*1/4 | 4 |
| 240 | 480 | 200 |   T4*1/4 | 4 |
