# 挂载vGPU的HPC产品和没有挂载HPC的产品性能对比

## Solidworks Benchmark
|  | Graphics(sec) | Procenssor(sec)） | I/O(sec) | Overall(sec) | Rendering(sec) | RealView Performance(sec) | Simulation(sec) |
|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|
| AMD EPYC 7542 32vcpu + Nvidia GRID T4-4Q | 26.6 | 37.2 | 35.5 | 99.4 | 7.1 | 21.5 | 90.9 |
| AMD EPYC 7542 32vcpu | 65.8 | 35.1 | 28.8 | 129.7 | 6.7 | - | 85.1 |

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
