# 性能对比vsCPU

## SPECviewperf 13 Benchmark基准测试
<p align="right">单位：fps</p>

|  | 3dsmax-06 | catia-05 | creo-02 | energy-02 | maya-05 | medical-02 | showcase-02 | snx-03 | sw-04 |
|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|
| AMD EPYC 7542 32vcpu + Nvidia GRID T4-4Q | 52.91 | 56.44 | 48.08 | 21.86 | 54.79 | 43.45 | 37.51 | 58.33 | 42.44 |
| AMD EPYC 7542 32vcpu | 2.02 | - | - | - | - | - | 1.07 | 0.01 | - |
<p align="right">(由于缺少GPU，CPU实例无法运行OpenGL相关测试)</p>
## Solidworks Benchmark基准测试
<p align="right">单位：sec</p>
1

|  | Graphics | Procenssor | I/O | Overall | Rendering | RealView Performance | Simulation |
|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|
| AMD EPYC 7542 32vcpu + Nvidia GRID T4-4Q | 26.6 | 37.2 | 35.5 | 99.4 | 7.1 | 21.5 | 90.9 |
| AMD EPYC 7542 32vcpu | 65.8 | 35.1 | 28.8 | 129.7 | 6.7 | - | 85.1 |

## Solidworks Visualize渲染测试
<p align="right">单位：sec</p>
<table align="center">
    <tr>
        <td colspan="2"></td><td>1000pass</td><td>100pass</td> 
    </tr>
    <tr>
        <td rowspan="2">AMD EPYC 7542 32vcpu + Nvidia GRID T4-4Q</td><td>CPU+GPU</td><td>128</td><td>13</td>
    </tr>
    <tr>
        <td>GPU</td><td>300</td><td>14</td>
    </tr>
    <tr>
        <td>AMD EPYC 7542 32vcpu</td><td>CPU</td><td>555</td><td>57</td>
    </tr>
</table>
