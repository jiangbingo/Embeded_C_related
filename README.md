# Embeded_C_related

### ARM、MCU、DSP、FPGA、SOC各是什么？区别是什么？

#### ARM

MCU本质为一片单片机，指将计算机的CPU、RAM、ROM、定时计数器和多种I/O接口集成在一片芯片上，形成的芯片级的计算机。

MCU做得好的厂商：瑞萨(Renesas)、恩智浦(NXP)、新唐、微芯(Microchip)、意法半导体(ST)、爱特梅尔(Atmel)、英飞凌(Infineon)、德州仪器(TI)、东芝(Toshiba)、三星(Samsung)、赛普拉斯(Cypress)、亚德诺半导体(ADI)、高通(Qualcomm)、富士通(Fujitsu)、超威半导体(AMD)、盛群/合泰半导体(Holtek)、中颖电子、炬力、华润微、沛城、义隆、宏晶、松翰、凌阳、华邦电子、爱思科微、十速科技、佑华微、应广、欧比特、贝岭、东软载波微、君正、中微、兆易、晟矽微、芯海、联华、希格玛、汇春、建荣科技、华芯微、神州龙芯、紫光微、时代民芯、国芯科技、中天微等等。

### DSP 
DSP(Digital SignalProcessing)，数字信号处理，简称DSP。DSP是用数值计算的方式对信号进行加工的理论和技术。另外DSP也是Digital Signal Processor的简称，即数字信号处理器，它是集成专用计算机的一种芯片，只有一枚硬币那么大。

### FPGA
FPGA(Field－Programmable Gate Array)，即现场可编程门阵列，它是在PAL、GAL、CPLD等可编程器件的基础上进一步发展的产物。它是作为专用集成电路(ASIC)领域中的一种半定制电路而出现的，既解决了定制电路的不足，又克服了原有可编程器件门电路数有限的缺点。

FPGA做得好的厂商：Altera((阿尔特拉)被Intel收购)、Xilinx(赛灵思)、Actel、Lattice(莱迪思)、Atmel、京微雅格、QuickLogic、Microsemi、Cypress、TI、上海复旦微、广东高云、同方国芯、西安智多晶、中国电子、成都华微、深圳国微、遨格芯等等。

### SOC
SoC的定义多种多样，由于其内涵丰富、应用范围广，很难给出准确定义。一般说来， SoC称为系统级芯片，也有称片上系统,意指它是一个产品，是一个有专用目标的集成电路，其中包含完整系统并有嵌入软件的全部内容。同时它又是一种技术，用以实现从确定系统功能开始，到软/硬件划分，并完成设计的整个过程。

## ARM、MCU、DSP、FPGA、SOC的比较

### 采用架构

* ARM：架构采用32位精简指令集（RISC）处理器架构，从ARM9开始ARM都采用了哈佛体系结构，这是一种将指令与数据分开存放在各自独立的存储器结构，独立的程序存储器与数据存储器使处理器的处理能力得到较大的提高。ARM多采用流水线技术，此技术通过多个功率部件并行工作来缩短程序执行时间，使指令能在多条流水线上流动，从而提高处理器的效率和吞吐率。现今ARM7采用了典型的三级流水线，ARM9采用五级流水线技术，而ARM11使用了7级流水线，ARM Cortex-A9更是使用了可变流水线结构（支持8-11级流水线）。在多核心的支持上ARM Cortex-A9最多可支持4个核心，这是ARM系列处理器中首次支持多核心技术。下图表示了ARM Cortex-A9的内部结构。

* MCU：大都在结构上是基于冯·诺伊曼结构的，这种结构清楚地定义了嵌入式系统所必需的四个基本部分：一个中央处理器核心，程序存储器（只读存储器或者闪存）、数据存储器（随机存储器）、一个或者更多的定时/计数器，还有用来与外围设备以及扩展资源进行通信的输入/输出端口——所有这些都被集成在单个集成电路芯片上。指令集上早期的MCU是采用CISC的，后面被RISC取代。在总线位数上，MCU覆盖了4位、8位、16位、32位，应用十分广泛。

* DSP：又名数字信号处理器，它是一种专用于实时的数字信号处理的微处理器。结构上它采用哈佛结构，同样采用流水线技术。此外，DSP被用于宿主环境时可作为直接内存存取设备运作，还支持从模拟数字转换器（ADC）获得数据，最终输出的是由数字模拟转换器（DAC）转换为模拟信号的数据，支持一定的并行处理。

* FPGA: FPGA是英文Field Programmable Gate Array（现场可编程门阵列）的缩写，它是在PAL、GAL、PLD等可编程器件的基础上进一步发展的产物，是专用集成电路（ASIC）中集成度最高的一种。FPGA采用了逻辑单元阵列LCA（Logic Cell Array）这样一个新概念，内部包括可配置逻辑模块CLB（Configurable Logic Block）、输出输入模块IOB（Input Output Block）和内部连线（Interconnect）三个部分。用户可对FPGA内部的逻辑模块和I/O模块重新配置，以实现用户的逻辑。它还具有静态可重复编程和动态在系统重构的特性，使得硬件的功能可以像软件一样通过编程来修改。FPGA有别于DSP、ARM、MCU的地方主要在于它的并行处理能力，它的强大并行性使复杂的运算得到极大的速度比提升。

* SOC:　系统芯片是一个将计算机或其他电子系统集成单一芯片的集成电路。系统芯片可以处理数字信号、模拟信号、混合信号甚至更高频率的信号。系统芯片常常应用在嵌入式系统中。系统芯片的集成规模很大，一般达到几百万门到几千万门。SOC相对比较灵活，它可以将ARM架构的处理器与一些专用的外围芯片集成到一起，组成一个系统。其实现有的ARM处理器如Hisi-3507、hisi3516等处理器都是一个SOC系统，尤其是应用处理器它集成了许多外围的器件，为执行更复杂的任务、更复杂的应用提供了强大的支持。


### 功耗           

* ARM: 可以说ARM之所以在移动市场上得到极大的成功，其中最主要的原因便是它的低功耗。众所周知的是在移动市场上的电子产品对处理器的功耗是十分敏感的，在过去PC平台上处理器的功耗在几十W到上百W不等，这样的功耗放在移动平台上是不可想像的，ARM在主频1G的情况下功耗才几百mW,强劲的低功耗使它能适应移动电子产品。

* DSP：在与非网的一组数据上显示，在数字信号处理方面的市场占有率DSP与FPGA各得半壁江山。DSP相对于FPGA的一个优势是它的功耗相对较低，DSP生产厂商通过提高处理器的主频、努力降低功耗来保证它的市场占有率，因为在高性能的数字处理市场上FPGA似乎更占有优势。如果单纯从DSP领域上来看，DSP在功耗上、性能上做得最好的要数TI公司，TI公司的DSP处理器相对其它的DSP厂商生产的处理器成本更低、功耗更低，所以TI的DSP芯片更在竞争力。

* MCU：MCU面世时间最长，各种厂商都有它们自己的架构与指令集，如果从低功耗方面来看，TI的MSP430型MCU做得相对较好。

* FPGA：FPGA由于它的内部结构原因造成它的功耗相对较高、芯片发热量大，这也是它的一个缺点。但这也是不可避免的，在支持高性能的并发计算数字电路，且内部的逻辑门大都采用标准的宽长比，最终生成的数字电路必然会在功耗上无法与ASIC等专用处理器比较。

* SOC：由于SOC自身的灵活性，它将多个器件集成到一个极小的芯片上从而组成一个系统，SOC系统相对于MCU等处理器组成的系统来说，它在功耗上具有优势。并且，SOC芯片可在版图层面上结合工艺、电路设计等因素对系统的功耗进行系统的优化，这样比由现今外围的PCB版搭建出来的系统功耗更低，占用面积更小。


### 速度

* ARM随着市场应用的需求提高，ARM厂商纷纷通过优化来提高它的主频，提升它的性能。从开始的100Mhz到惊人的2.3Ghz，ARM主频以惊人的速度向前发展。

* DSP现今最快的主频能达到1.2Ghz。当然不能单纯从主频判断它的性能会比ARM差，DSP具有单时钟周期内完成一次乘法和一次加法的能力，一般的ARM不具备这样的能力，DSP在计算领域优势尤其明显，所以TI结合了ARM和DSP两者的优势，生产出达芬奇异构芯片，当然这是属于SOC的范畴了。

* MCU作为低端的应用处理器，它的主频从数M到几十Mhz不等。

* FPGA主频时钟最高可达几Ghz甚至上10Ghz，当然它的成本也不菲。如果将FPGA与ARM、DSP等作为比较，从主频上进行比较是没有多大意义的，毕竟并行计算的能力要远远超出一般通用的处理器采用的串行计算几十倍。如同样的一个滤波算法在主频为100Mhz的FPGA上实现要比在主频为1Ghz的ARM上实现仍要快。


### 应用与市场           

* ARM处理器现在主要是三个系列分别为A系列、R系列、M系列，其中A系列主攻消费电子应用，应用十分广泛。
```
计算：上网本、智能本、输入板、电子书阅读器、瘦客户端
手机：智能手机、特色手机
数字家电：机顶盒、数字电视、蓝光播放器、游戏控制台
汽车：信息娱乐、导航
企业：激光打印机、路由器、无线基站、VOIP 电话和设备
无线基础结构：Web 2.0、无线基站、交换机、服务器
`
R系列处理器主要针对一些对实时性要求较高的应用，如航空航天、汽车电子等场合，它具备高可靠性、高可用性、高容错能力、实时响应等优点。

M系列处理器主要针对较低端的应用，它的最初目标是替换现有的市面上的MCU。
ARM Cortex-M0
ARM Cortex-M0+
ARM Cortex-M3
ARM Cortex-M4
“8/16 位”应用
“8/16 位”应用
“16/32 位”应用
“32 位/DSC”应用
低成本和简单性
低成本，最佳能效
高性能，通用
有效的数字信号控制
 ```


* DSP主要针对一些计算能力要求较高的应用，如视频图像处理、智能机器人、数字无线、宽带访问、数字音频、高分辨率成像和数字电机控制等。

* MCU应用最为广泛，主要利益于它的成本控制上，使它能在许多对计算能力要求不那么高的应用立足。相信在未来几年里，MCU市场关键增长驱动力将来自于绿色能源，智能电子设备，智能电网以及电子产品的升级换代比如汽车电子。

* SOC应用也十分广泛，主要是因为现有主流ARM芯片采用的架构便是SOC架构的一种，SOC是一个比较广泛的概念，现阶段许多ARM、DSP都开始采用SOC的方式来将多个器件加到处理器上组成复杂的系统。

### 开发成本

* ARM主要是搭载LINUX、ANDROID、WINCE等操作系统，在开发难度上看，相对MCU、DSP较难入门，它需要开发人员对操作系统有较深的了解；从成本来看，ARM的单芯片成本较MCU要高，主要还是应用于一些较为复杂的系统上。

* MCU入门最容易，上手也快，开发难度较小，并且它的成本低，在低端市场应用最为广泛。

* DSP入门较容易，但单芯片成本较高，主要还是应用于对计算能力要求高的应用。当然DSP也可以搭载操作系统，搭载操作系统后可适用于多任务的应用上。

* FPGA的开发难度较大并且开发周期也相对较长，此外它的单芯片成本很高。