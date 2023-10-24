![](https://github.com/d2l-ai/d2l-en/actions/workflows/ci.yml/badge.svg#id=ZWV0W&originHeight=20&originWidth=205&originalType=binary&ratio=1&rotation=0&showTitle=false&status=done&style=none&title=) ![](https://github.com/d2l-ai/d2l-en/actions/workflows/build-docker.yml/badge.svg#id=MnbR1&originHeight=20&originWidth=180&originalType=binary&ratio=1&rotation=0&showTitle=false&status=done&style=none&title=)
> **Original URL：**[**https://github.com/chenzomi12/DeepLearningSystem**](https://github.com/chenzomi12/DeepLearningSystem)
> **文字课程开源在 **[**AISys**](https://chenzomi12.github.io/)**，系列视频托管**[**B站**](https://space.bilibili.com/517221395)**和**[**油管**](https://www.youtube.com/@zomi6222/videos)**，PPT开源在 **[**github**](https://github.com/chenzomi12/DeepLearningSystem)
> **建议到 **[**Releases · chenzomi12/DeepLearningSystem**](https://github.com/chenzomi12/DeepLearningSystem/releases)** 来下载需要的内容**

<a name="1495fa52"></a>
## 项目背景
这个开源项目英文名字叫做 **Deep Learning System** 或者 **AI System(AISys)**，中文名字叫做 **深度学习系统** 或者 **AI系统**。本开源项目主要是跟大家一起探讨和学习人工智能、深度学习的系统设计，而整个系统是围绕着 ZOMI 在工作当中所积累、梳理、构建 AI 系统全栈的内容。希望跟所有关注 AI 开源项目的好朋友一起探讨研究，共同促进学习讨论。
<a name="3de1c8fb"></a>
## 课程内容大纲
**先修课程:** C++/Python，计算机体系结构，人工智能基础<br />第一部分，AI基础知识和AI系统的全栈概述的**AI系统概述**，以及深度学习系统的系统性设计和方法论，主要是整体了解AI训练和推理全栈的体系结构内容。<br />第二部分，硬核篇介绍**AI芯片**，这里就很硬核了，从芯片基础到AI芯片的范围都会涉及，芯片设计需要考虑上面AI框架的前端、后端编译，而不是停留在天天喊着吊打英伟达，被现实打趴。<br />第三部分，进阶篇介绍**AI编译器原理**，将站在系统设计的角度，思考在设计现代机器学习系统中需要考虑的编译器问题，特别是中间表达乃至后端优化。<br />第四部分，实际应用**推理系统**，讲了太多原理身体太虚容易消化不良，还是得回归到业务本质，让行业、企业能够真正应用起来，而推理系统涉及一些核心算法和注意的事情也分享下。<br />第五部分，介绍**AI框架核心技术**，首先介绍任何一个AI框架都离不开的自动微分，通过自动微分功能后就会产生表示神经网络的图和算子，然后介绍AI框架前端的优化，还有最近很火的大模型分布式训练在AI框架中的关键技术。<br />第六部分，汇总篇介绍**大模型**，大模型是全栈的性能优化，通过最小的每一块AI芯片组成的AI集群，编译器使能到上层的AI框架，中间需要大量的集群并行、集群通信等算法在软硬件的支持。

| 编号 | 名称 | 具体内容 |
| --- | --- | --- |
| ** AI系统概述** |  |  |
| 1 | [AI 系统](./010System/) | 算法、框架、体系结构的结合，形成AI系统 |
| 1 | [AI 计算体系](./021HW_Foundation/) | 神经网络等AI技术的计算模式和计算体系架构 |
| **AI芯片体系结构** |  |  |
| 2 | [AI 芯片基础](./022HW_ChipBase/) | CPU、GPU、NPU等芯片体系架构基础原理 |
| 3 | [图形处理器 GPU](./023HW_GPUBase/) | GPU的基本原理，英伟达GPU的架构发展 |
| 4 | [英伟达 GPU 详解](./024HW_NVIDIA/) | 英伟达GPU的TensorCore、NVLink深度剖析 |
| 5 | [国外 AI 处理器](./025HW_Abroad/) | 谷歌、特斯拉等专用AI处理器核心原理 |
| 6 | [国内 AI 处理器](./026HW_Domestic/) | 寒武纪、燧原科技等专用AI处理器核心原理 |
| AI编译原理 |  |  |
| 1 | [传统编译器](./031CM_Tradition/) | 传统编译器GCC与LLVM，LLVM详细架构 |
| 2 | [AI 编译器](./032CM_AICompiler/) | AI编译器发展与架构定义，未来挑战与思考 |
| 3 | [前端优化](./033CM_Frontend/) | AI编译器的前端优化(算子融合、内存优化等) |
| 4 | [后端优化](./034CM_Backend/) | AI编译器的后端优化(Kernel优化、AutoTuning) |
| 5 | 多面体 | 待更ing... |
| 6 | [PyTorch2.0](./036CM_PyTorch/) | PyTorch2.0最重要的新特性：编译技术栈 |
| AI推理系统 |  |  |
| 1 | [推理系统](./041INF_Inference/) | 推理系统整体介绍，推理引擎架构梳理 |
| 2 | [轻量网络](./042INF_Mobilenet/) | 轻量化主干网络，MobileNet等SOTA模型介绍 |
| 3 | [模型压缩](./043INF_Slim/) | 模型压缩4件套，量化、蒸馏、剪枝和二值化 |
| 4 | [转换&优化](./044INF_Converter/) | AI框架训练后模型进行转换，并对计算图优化 |
| 5 | [Kernel优化](./045INF_Kernel/) | Kernel层、算子层优化，对算子、内存、调度优化 |
| **AI框架核心技术** |  |  |
| 1 | [AI框架基础](./021FW_Foundation/) | AI框架的作用、发展、编程范式 |
| 2 | [自动微分](./022FW_AutoDiff/) | 自动微分的实现方式和原理 |
| 3 | [计算图](./023FW_DataFlow/) | 计算图的概念，图优化、图执行、控制流表达 |
| 大模型训练（待整理） |  |  |
| 4 | [分布式集群](./061FW_AICluster/) | AI集群服务器架构、软硬件通信方式 |
| 5 | [分布式算法](./062FW_AIAlgo/) | 大模型挑战，Transformer和MOE结构的大模型 |
| 6 | [分布式并行](./063FW_Parallel/) | 数据并行、模型并行、混合并行的原理和策略 |

