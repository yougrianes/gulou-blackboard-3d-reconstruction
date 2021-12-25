# 鼓楼黑板-3d-reconstruction

# gulou-blackboard-3d-reconstruction

此项目计划使用传统计算机视觉方法，利用互联网收集的图片，对南京大学鼓楼校区中南园教学楼花坛前侧的黑板进行3d重建。

这是一个个人的兴趣项目。欢迎有兴趣的同学一起参与到项目的讨论和开发。工作很忙，下班和周末有空会写一写，项目进展不定期。

## Introduction
最近学校的鼓楼校区南园的黑板被拆掉了，心里还是蛮难受的。正好自己所做的工作是计算机视觉相关，所以想着能不能在自己的专业上为学校的同学老师们帮一些忙。

众所周知，计算机视觉的应用是很广泛的。其中一个比较常见的应用是利用立体视觉进行三维重建，例如对一些文物进行数字存档和实地测量。在几年前的巴黎圣母院失火事件中，育碧在其制作的游戏：*Assassin’s Creed Unity*中，对巴黎圣母院的建模也一定程度上对文物的信息起到了保护作用。取决于实地测量和对信息进行存档的精细程度，倘若文物因为人为或者是自然灾害（如地震、洪水、酸雨、闪电等）而受到损毁，这些珍贵的数字信息将对文物修复与重建工作提供宝贵的参考资料。

通常来说，这些勘探与测量工作是专业而且复杂的，但随着现在获取信息的日渐便捷，例如互联网图片等，这些蕴含着大量有用信息的资料应当被有效的利用起来。计算机视觉中的三维重建领域中的技术，例如从运动到结构（Structure-from-Motion）、多目视觉下的相机参数恢复、点云匹配等，是一个可以尝试的方式。本项目想要做的事情是通过网络上能够获取的图片以及其他渠道的资料，对现在已经损坏的鼓楼校区的黑板进行三维重建，抢救性的还原一些原始信息。在工作实时进展的基础之上，希望能够基于三维重建得到的网格模型或点云信息的基础之上，进行三维建模的工作，从而得到一个完成度比较高的3d模型。

我当前的预期是这个模型应该是一个可以被例如3dmax、blender等三维建模软件可以兼容和导入的格式，从而为后续的工作留下更多的可能性，例如用来构造一些环境场景，并且引入一些交互。这通常用在例如游戏的地图环境渲染之中，等等。这些工作已经有比较成熟的应用，有成熟和开放的软件可以使用。这种方法应该不仅是黑板，而应该是一种可以运用到多个场景中的工具或者通用方法。

## 设计方案
预期的输入：

· 一定数量的图片。最好是包含RGB三个颜色通道的彩色图片。有标定参数最好，但是通常来说是没有的。
· 有连续图片的视频流。颜色是彩色的。

预期得到的结果：是一个colored mesh。


### 论文引用和参考资料
http://media.gisera.com/jsjl/show/329.aspx

Y. Furukawa, J. Ponce, Accurate camera calibration from multi-view stereo and bundle adjustment, Int. J. Comput. Vision, 84 (2009) 257-268.

https://zhuanlan.zhihu.com/p/76047709

Occluding Contours for Multi-View Stereo, http://grail.cs.washington.edu/projects/sq_rome_g2/

https://zhuanlan.zhihu.com/p/158097602
