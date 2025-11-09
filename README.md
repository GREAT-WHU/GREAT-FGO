# GREAT-FGO
GREAT-FGO: 武汉大学GREAT团队因子图优化导航软件（1.0版）
概述
GREAT (GNSS+ REsearch, Application and Teaching) 软件由武汉大学测绘学院设计开发，是一个用于空间大地测量数据处理、精密定位和定轨以及多源融合导航的综合性软件平台。
  GREAT-FGO是GREAT软件中的一个重要模块，主要用于因子图优化 (Factor Graph Optimization, FGO) 导航解算，包括RTK、RTK/INS、RTK/INS/Visual、RTK/INS/Visual/Lidar以及PPP、PPP/INS、PPP/INS/Visual等多种算法。软件中，核心计算模块使用C++语言编写，辅助脚本模块使用Python3语言实现结果绘制。GREAT-FGO软件使用CMake工具进行编译管理，用户可以灵活选择GCC、Clang、MSVC等主流C++编译器。目前支持在Windows下编译运行，Linux系统需要用户自行编译测试。
  GREAT-FGO由2个可移植程序库组成，分别是LibGREAT和LibGnut。除了原GREAT-PVT中的GNSS定位解决方案、GREAT-MSF提供的多传感器融合导航功能外，GREAT-FGO提供了基于因子图优化的RTK与RTK/INS紧耦合算法。
  本次开源的GREAT-FGO 1.0版本支持以下功能：

	1.支持GPS、GLONASS、Galileo、BDS-2/3等卫星导航系统
	
	2.支持基于因子图优化的RTK解算
	
	3.支持基于因子图优化的RTK/INS紧耦合解算，支持载波相位模糊度固定
	
	4.支持组合系统动态快速初始化，包括位移矢量和速度矢量辅助对准
	
	5.支持自定义IMU数据格式、噪声模型
	
	6.软件包还提供定位结果绘图脚本，便于用户对数据进行结果分析


  为服务大地测量与导航领域的青年学子，现开源GREAT软件基于因子图优化的RTK与RTK/INS部分的代码。不足之处恳请批评指正，我们将持续完善。后面会陆续开源更多传感器融合，包括相机、激光雷达、高精地图、超宽带等，同时开展系列代码培训。

软件包目录结构
GREAT-MSF_1.0
  ./src	                 源代码 *
    ./app                  GREAT-PVTFGO、GREAT-GINSFGO、GREAT-MSF和GREAT-PVT主程序 *
    ./LibGREAT             因子图优化核心算法库 *
    ./LibGnut              Gnut库 *
    ./Third-party          第三方库 *
  ./sample_data          算例数据 *
  ./plot                 绘图工具 *
  ./doc                  GREAT-FGO相关文档 *
  
  安装和使用
参见《GREAT-FGO说明文档_1.0.pdf》或关注我们团队后续在视频网站bilibili发布的讲解视频。

参与贡献
开发人员：

武汉大学GREAT团队, Wuhan University.

三方库：
	GREAT-FGO使用G-Nut库（http://www.pecny.cz/）Copyright (C) 2011-2016 GOP - Geodetic Observatory Pecny, RIGTC
	
	GREAT-FGO使用pugixml库（http://pugixml.org）Copyright (C) 2006-2014 Arseny Kapoulkine
	
	GREAT-FGO使用Newmat库（http://www.robertnz.net/nm_intro.htm）Copyright (C) 2008: R B Davies
	
	GREAT-FGO使用spdlog库（https://github.com/gabime/spdlog）Copyright(c) 2015-present, Gabi Melman & spdlog contributors
	
	GREAT-FGO使用GLFW库(https://www.glfw.org/) Copyright (C) 2002-2006 Marcus Geelnard, Copyright (C) 2006-2019 Camilla Löwy
	
	GREAT-FGO使用Eigen库（https://eigen.tuxfamily.org）Copyright (C) 2008-2011 Gael Guennebaud
	
	GREAT-FGO使用PSINS库(https://psins.org.cn) Copyright(c) 2015-2025 Gongmin Yan
	
	GREAT-FGO使用Ceres 库(http://ceres-solver.org/)	Copyright 2023 Google Inc.

下载地址
GitHub：https://github.com/GREAT-WHU/GREAT-FGO

其它
欢迎加入QQ群(1009827379)参与讨论与交流。

微信公众号：GREAT智能导航实验室，我们将持续推送团队成果。

bilibili账号：GREAT智能导航实验室，我们将持续发布软件讲解视频。
