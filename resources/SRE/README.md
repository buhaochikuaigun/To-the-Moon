# SRE

虽然个人感觉十个 IT 志向的留学生里也不一定有一个 SRE/Devops/Infra 方向的，但是既然 PM 也有人写，那就写一下 SRE。

## SRE 是什么岗位？

首先关于 SRE 的职能或者定位，可以询问 ChatGPT 或者查阅群友某次向 SDE 朋友[介绍 SRE 概念和 DevOps 时的 slide](https://docs.google.com/presentation/d/1fsPwH3xt7NZChs2TGgpnc4CqRLl_QSnpFE-Yowq23zQ/edit#slide=id.p)，分享的录像还没想好适不适合发。

简单的说，SRE 负责代码写好以前和写好以后的一切事情：
- 开发平台
- 部署管道
- 生产环境
- 发布运维
- etc

而在日本，SRE 在大部分情况下约等于使用各大公有云，只有到了 LINE 和乐天这个体量会开始自己研发云平台。

再功利性一点地说，SRE 适合：
- 不喜欢写太多代码的
- 不怕 oncall 的
- 知识体系宽而杂的
- 擅长使用各种新工具的

需要和 solution engineer 或者 support engineer 区分的是，SRE 一般是负责本家公司的固定业务线，不涉及业务外包和技术解决方案/服务销售和售后支持。

## 什么样的公司需要 SRE？

一言以蔽之：规模不太大也不太小的公司。

这么概括看起来很抽象又不是那么准确，但这是因为公司在发展的不同阶段对 deployment 和 operation 有不同程度的要求：
- 太小的公司可能开发人员写写脚本就部署了，挂了重启大部分时候就好了，很少需要专门的 SRE 负责
- MAGA 的自有系统完善性很大程度上自动化和标准化了各种流程，基础设施有足够的冗余度，SRE 不需要分布在各个业务线里

而中小型公司一般因为发展阶段而：
- 需要一定程度的团队协作，需要设立标准对开发部署流程进行规范和标准化建设
- 对产品服务的可用性开始有要求
- 云服务很贵，需要合理的容量规划

在日本，在招聘 SRE/DevOps/Infrastructure Engineer 的公司据我了解有：
- Line
- 乐天
- PFN
- CyberAgent
- Mercari

以上公司的此类岗位接受新卒投递，有此类岗位但没有明确是否要求有相关经验的公司有：

- Bloomberg
- Apple
- Paypay
- Indeed
- Woven
- 和各种小公司

## SRE 需要学习什么？

简单且很武断的个人判断，SRE ≈ (50%~80% coding skill + 130%~150% system / networking skill + Cloud knowledge) of SDE，不一定准确，各家公司的考察方式不尽相同，但是大致意思是对 coding 要求低一些但是经常会问一些 why 的问题。

### 了解 Unix,Linux 操作系统 和计算机网络基础 

1. 我们为什么要使用 Unix/Linux，了解 Unix/Linux 基本结构
2. 了解我们的互联网的基本结构，尤其是分层模型，这对我们管理服务器至关重要
 
参考资料     

1. [维基百科](https://zh.wikipedia.org/wiki/%E6%93%8D%E4%BD%9C%E7%B3%BB%E7%BB%9F)      
2. [操作系统原理及应用](http://c.biancheng.net/cpp/u/xitong/)
3. 《图解 TCP/IP》
4. 任意版本的《计算机网络》

### Shell 脚本编程和 Linux 下各种工具
	
1. Shell 脚本入门
2. 学习如何使用各种工具管理服务器	

参考资料 

1. 《高级 Bash 脚本编程指南》（[HTML version on TLDP](http://tldp.org/LDP/abs/html/)）
2. [极客学院 Wiki](http://wiki.jikexueyuan.com/project/shell-tutorial/shell-brief-introduction.html)
3. [Linux 工具快速教程](http://linuxtools-rst.readthedocs.org/zh_CN/latest/index.html)
4. [Google shell style guide](http://zh-google-styleguide.readthedocs.io/en/latest/google-shell-styleguide/background/)


### SDE 基础

- 至少一门 OOP 语言，推荐 Python （大量运维小工具基于 Python），可选 Rust 和 Golang。
- System Design 参见 [SDE](./SDE/README.md)
  
### 公有云知识

参见各大公有云自己的认证培训材料，推荐自己动手玩一玩，各大公有云都有免费试用。