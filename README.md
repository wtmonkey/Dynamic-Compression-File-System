# HelloWorld
基于UNIX/Linux的动态压缩文件系统

课题需求：

    本次课题题目是“基于Unix/Linux的模拟动态压缩文件系统”，用程序模拟文件系统的运行，实现文件系统基本功能，在这个基础上，进一步实现动态压缩管理。具体是系统能够自发的对文件按照一定的规则实现管理，如按照文件的大小或者是文件是使用频率，对于超过一定大小或者是低于一定是用频率的文件，系统自动的选择压缩储存，对于低于一定大小或者是高于一定是用频率的文件，系统自动选择普通储存方式，此过程完全对用户透明由系统自发完成，频率参数和大小选择由菜单方式提供用户自自己选择。

课题前景及创新点：

    在嵌入式Linux系统中，文件系统是构建嵌入式Linux系统的重要组成部分,是Linux/Unix系统不可或缺的组件。随着数据的爆炸式增长储存行业已经发生了翻天覆地的变化，文件系统如何才能紧跟时代步伐，满足越来越高要求的储存需求呢？硬盘的成本容量几乎每年以40%的速度增长，现在市场上已经可以看到容量为2TB的机械硬盘，但他们的性能却没能按比例提高，固态硬盘出现解决了传统硬盘的许多弊病，因此未来几年势必会有一场关于储存的技术革命文件系统也需要为储存革命做好准备，而储存的效率必然成为其中一个关键问题。本次课题主要考虑文件系统对文件的管理，充分提高储存空间利用率，效率的提高意味着，对空间大小的需求降低，对开发成本和条件都是有所改善的。降低开发难度。更加有利于Linux的发展和创新。
    现如今，对于储存效率的要求更加关注，本次课题就是针对内存利用率以及用户体验的多方面综合考虑，提供文件动态压缩储存方案，在用户体验不至于受到明显破坏的情况下，充分高效的利用文件储存空间，即满足了公司降低成本长远发展的需求，又不至于降低用户体验，导致市场丢失。

技术路线：

    根据实际linux文件系统层次结构，以linux文件系统磁盘组织为依据，开辟一块储存区，模拟文件储存空间，创建索引节点，文件实际储存，目录等等数据结构。再分析程序流程，构建文件系统基本功能程序流程图，然后代码具体实现各个功能模块现。实现普通简单文件系统后，用shell脚本，实现用户参数选择界面，为文件系统管理提供标准支持。最后管理程序捕获参数，系统扫描特定区域，或特定权限文件，实现动态管理。
    
总体过程为:

    模拟常规简单linux文件系统-->实现动态压缩函数和文件信息提取函数-->shell界面参数提取-->实现动态文件系统管理

平台：ubuntu12.04
