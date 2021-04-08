# 性能对比vsCPU

## SPECviewperf®13 Benchmark基准测试
<p align="right">单位：fps</p>

|  | 3dsmax-06 | catia-05 | creo-02 | energy-02 | maya-05 | medical-02 | showcase-02 | snx-03 | sw-04 |
|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|
| AMD EPYC 7542 32vcpu + Nvidia GRID T4-4Q | 52.91 | 56.44 | 48.08 | 21.86 | 54.79 | 43.45 | 37.51 | 58.33 | 42.44 |
| AMD EPYC 7542 32vcpu | 2.02 | - | - | - | - | - | 1.07 | 0.01 | - |
<p align="right">(由于缺少GPU，CPU实例无法运行OpenGL相关测试)</p>

SPECviewperf®13基准测试是SPEC标准化评测组织发布的基于专业应用程序测量图形性能的基准测试。该基准测试在OpenGL和Direct X应用程序编程接口下，模拟了各种作图、渲染软件的应用，从而测试GPU的3D图形性能。从测试结果可以看出，挂在了vGPU的实例在一些科学软件的作图和渲染方面的应用远高于仅有CPU的实例。

## SolidWorks Benchmark基准测试
<p align="right">单位：sec</p>

|  | Graphics | Procenssor | I/O | Overall | Rendering | RealView Performance | Simulation |
|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|
| AMD EPYC 7542 32vcpu + Nvidia GRID T4-4Q | 26.6 | 37.2 | 35.5 | 99.4 | 7.1 | 21.5 | 90.9 |
| AMD EPYC 7542 32vcpu | 65.8 | 35.1 | 28.8 | 129.7 | 6.7 | - | 85.1 |

![avatar](melo-zs/vgpu/benchmark.jpg)

SolidWorks是制造业广泛流行的3D CAD设计软件，使用软件自带的性能基准测试得出以上结果。CPU实例不支持RealView特性，因此空缺一项测试成绩。测试结果表明在图形方面，挂载vGPU的实例要远优于CPU实例

## SolidWorks Visualize渲染测试
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

SolidWorks Visualize是SolidWorks提供的用于工业设计、产品设计的一款专业的渲染工具。图表中Pass表示渲染中的通道数，从测试结果可以看出在渲染较高画质的图像时，使用CPU+GPU混合模式的渲染速度比只用CPU快将近5倍。
