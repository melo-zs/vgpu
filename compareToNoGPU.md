# 挂载vGPU的HPC产品和没有挂载HPC的产品性能对比

## Solidworks Benchmark基准测试
<p align="right">单位：sec</p>
|  | Graphics(sec) | Procenssor(sec) | I/O(sec) | Overall(sec) | Rendering(sec) | RealView Performance(sec) | Simulation(sec) |
|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|
| AMD EPYC 7542 32vcpu + Nvidia GRID T4-4Q | 26.6 | 37.2 | 35.5 | 99.4 | 7.1 | 21.5 | 90.9 |
| AMD EPYC 7542 32vcpu | 65.8 | 35.1 | 28.8 | 129.7 | 6.7 | - | 85.1 |

## SPECviewperf 13 Benchmark基准测试
<p align="right">单位：fps</p>
|  | 3dsmax-06 | catia-05 | creo-02 | energy-02 | maya-05 | medical-02 | showcase-02 | snx-03 | sw-04 |
|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|
| AMD EPYC 7542 32vcpu + Nvidia GRID T4-4Q | 52.91 | 56.44 | 48.08 | 21.86 | 54.79 | 43.45 | 37.51 | 58.33 | 42.44 |
| AMD EPYC 7542 32vcpu | 2.02 | - | - | - | - | - | 1.07 | 0.01 | - |

<table>
    <tr>
        <td>列一</td> 
        <td>列一</td> 
   </tr>
    <tr>
        <td colspan="2">AMD EPYC 7542 32vcpu + Nvidia GRID T4-4Q</td>    
    </tr>
    <tr>
        <td colspan="2">AMD EPYC 7542 32vcpu</td>    
    </tr>
</table>
