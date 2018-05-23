---
title: 201 principles of software development
date: 2018-05-21 23:30:26
tags:
- software
- engineer
categories:
- software engineering
---
## 软件开发中的201条原则
本文翻译自《201 principles of software development》

--------------------------基本原则----------------------------

6. 可靠性差比效率低更可怕。

--------------------------需求分析----------------------------



--------------------------软件设计----------------------------

61. 把需求文档转变成设计文档并不是一件容易的事儿
62. 跟踪每一个需求，记录每一个需求的设计及实现情况（可以用表格来记录）
63. 评估每一种方案，从中选出最好的
64. 没有文档的设计不算真正的设计
65. 封装，便于维护以及隔离错误
66. 不要重复造轮子
67. KISS(Keep It Simple, Stupid)原则，即 保持简洁和单纯
68. 避免过多的特殊情况：如果需要考虑的特殊情况太多，说明设计或算法有问题
69. 最小化计算机世界与现实世界的距离，即 在选择模型和方法时尽可能地模拟现实世界
70. 保持设计的智能可控性，本质上是倡导分层设计，并提供多种视角 (->80)
71. 保持概念完整性，包括数据结构的组织、模块间的通信方式、错误警告等等的一致性。即使是由多个人开发的系统，看起来也像一个人开发的一样。
72. 概念错误比语法错误更重要、更难以排查。
73. 松耦合，高内聚
74. 为改变而设计，即 所作的设计必须能够适应变化的需求：模块化、可移植、可扩展、贴近现实(69)、智能可控(70)、概念完整(71)
75. 设计需要考虑后期维护。就可维护性而言，架构的选择比算法和代码更重要。
76. 设计需要考虑错误情况。尽量做到：
		1. 不引入错误
		2. 引入的错误很容易检测到
		3. 部署后依然存在的错误要么不重要，要么能够避免执行过程中出现灾难性问题
	有些具体方法可以帮助提高设计的鲁棒性：
		1. 不要遗漏任何一种状态，例如一个变量有4种取值，不要只检查其中的3种
		2. 预测尽可能多的“impossible”的情况，并给出恢复策略
		3. 为了排除引发灾难的情况，使用故障树(fault tree)分析预测不安全的情形
77. 构建通用性软件。通用性强的软件/组件一般运行会稍微慢一些。
78. 构建灵活性软件。灵活性强的组件一般比通用性强的组件运行更高效。
79. 使用高效的算法。要求设计者了解各种算法并能够进行算法复杂度分析。
80. 模块规格说明应该包含用户需要的所有信息，不要加入用户不需要的任何信息。即模块化。
81. 设计是多维度的，包括 打包(packaging, what is part of what), 分层(hierarchy, who needs whom), 调用(invocation, who invokes whom), 流程(processes)...
82. 伟大的设计来自于伟大的设计者
83. 了解你的应用程序，例如压力环境下的预期行为、输入频率、响应时间、天气的影响...等等
84. 可以复用一些模块或组件，因为复用的成本小且效率高。
85. 对于软件来说"garbage in, garbage out"是不正确的。对于无效的输入，软件应该给出智能的回应，指出为什么无效；并且不应该进行处理，而是返回错误码，避免错误向后扩散。
86. 可以通过冗余来实现软件可靠性：
		1. 并行策略，例如mr任务，每一个分片job都会起多个相同的、互不影响task，如果其中一个跑完了，就可以kill掉其他的了
		2. 冷备，当主控机器出现硬件故障时，可以启动备用机器继续提供服务
	软件的高可靠性需要很高的代价，有时针对一套需求可能需要提供两套设计方案。
87. 



> refer:《201 principles of software development》