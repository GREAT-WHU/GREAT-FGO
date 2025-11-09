# GREAT-FGO: Factor Graph Optimization-Based Positioning and Navigation Software by Wuhan University GREAT Group (Beta)

## Overview

  The GREAT (GNSS+ **RE**search, **A**pplication and **T**eaching) software suite is designed and developed by the School of Geodesy and Geomatics, Wuhan University. It is a comprehensive platform for space geodesy data processing, precise positioning and orbit determination, as well as multi-source fusion navigation. <br />
  GREAT-FGO is a key module within the GREAT software, dedicated to Factor Graph Optimization (FGO) based navigation solutions. It supports a variety of algorithms including RTK, RTK/INS, and multi-sensor fusion. In the software, core computation modules are implemented in C++, while auxiliary Python 3 scripts are provided for plotting results. GREAT-FGO uses CMAKE for build management, allowing users to flexibly choose mainstream C++ compilers such as GCC, Clang, and MSVC. It currently supports build and execution on Windows; for Linux, users are encouraged to compile and test locally. <br />
  GREAT-FGO consists of two portable program libraries: LibGREAT and LibGnut. In addition to the GNSS positioning solutions from the original GREAT-PVT and the multi-sensor fusion navigation capabilities provided by GREAT-MSF, GREAT-FGO delivers RTK and tightly-coupled RTK/INS algorithms based on factor graph optimization. <br />
  This open-sourced GREAT-FGO version 1.0 supports the following capabilities:
  

1.Supports RTK positioning based on factor graph optimization with carrier phase ambiguity resolution

2.Supports tightly-coupled RTK/INS integration based on factor graph optimization, featuring dynamic rapid initialization capability for integrated systems

3.Supports satellite navigation systems including GPS, GLONASS, Galileo, BDS-2/3

4.Supports custom IMU data formats and noise models

5.Support for trajectory visualization and Google Maps viewing

6.The software package also provides plotting scripts for positioning results to facilitate user data analysis


## Package Directory Structure

```shell
GREAT-FGO_1.0
  ./src                   Source code *
    ./app                 Main programs of GREAT-PVTFGO, GREAT-GINSFGO, GREAT-MSF and GREAT-PVT *
    ./LibGREAT            Core algorithm library for Factor Graph Optimization*
    ./LibGnut             Gnut library *
    ./Third-party         Third-party libraries *
  ./sample_data           Example datasets *
  ./plot                  Plotting utilities *
  ./doc                   Documentation related to GREAT-FGO *
```

## Installation and Usage

See **GREAT-FGO Documentation.pdf** included in the **./doc** directory.


## Contributing

Developers:

Wuhan University GREAT Team, Wuhan University.

Third-party libraries:

* GREAT-FGO uses the G-Nut library ([http://www.pecny.cz](http://www.pecny.cz))
  Copyright (C) 2011–2016 GOP - Geodetic Observatory Pecny, RIGTC.

* GREAT-FGO uses the pugixml library ([http://pugixml.org](http://pugixml.org))
  Copyright (C) 2006–2014 Arseny Kapoulkine.

* GREAT-FGO uses the Newmat library ([http://www.robertnz.net/nm_intro.htm](http://www.robertnz.net/nm_intro.htm))
  Copyright (C) 2008: R B Davies.

* GREAT-FGO uses the spdlog library ([https://github.com/gabime/spdlog](https://github.com/gabime/spdlog))
  Copyright (C) 2015–present, Gabi Melman & spdlog contributors.

* GREAT-FGO uses the GLFW library ([https://www.glfw.org](https://www.glfw.org))
  Copyright (C) 2002–2006 Marcus Geelnard, Copyright (C) 2006–2019 Camilla Löwy

* GREAT-FGO uses the Eigen library ([https://eigen.tuxfamily.org](https://eigen.tuxfamily.org))
  Copyright (C) 2008–2011 Gael Guennebaud

* GREAT-FGO uses the PSINS library ([https://psins.org.cn](https://psins.org.cn))
  Copyright (c) 2015–2025 Gongmin Yan

* GREAT-FGO uses the Ceres library ([http://ceres-solver.org](http://ceres-solver.org))
  Copyright 2023 Google Inc.

## Download

GitHub: [https://github.com/GREAT-WHU/GREAT-FGO](https://github.com/GREAT-WHU/GREAT-FGO)

## Others

You are welcome to join the QQ group (1009827379) for discussion and exchange.

WeChat Official Account: **GREAT智能导航实验室** — we will continue to share team updates.

bilibili Account: **GREAT智能导航实验室** — we will continue to publish software walkthrough videos.

---





# GREAT-FGO: 武汉大学GREAT团队基于因子图优化的定位导航解算软件（Beta版）

## 概述

&emsp;&emsp;GREAT (GNSS+ REsearch, Application and Teaching) 软件由武汉大学测绘学院设计开发，是一个用于空间大地测量数据处理、精密定位和定轨以及多源融合导航的综合性软件平台。<br />
&emsp;&emsp;GREAT-FGO是GREAT软件中的一个重要模块，主要用于因子图优化 (Factor Graph Optimization, FGO) 导航解算，包括RTK、RTK/INS与多传感器融合等多种算法。软件中，核心计算模块使用C++语言编写，辅助脚本模块使用Python3语言实现结果绘制。GREAT-FGO软件使用CMake工具进行编译管理，用户可以灵活选择GCC、Clang、MSVC等主流C++编译器。目前支持在Windows下编译运行，Linux系统需要用户自行编译测试。<br />
&emsp;&emsp;GREAT-FGO由2个可移植程序库组成，分别是LibGREAT和LibGnut。除了原GREAT-PVT中的GNSS定位解决方案、GREAT-MSF提供的多传感器融合导航功能外，GREAT-FGO提供了基于因子图优化的RTK与RTK/INS紧耦合算法。<br />
&emsp;&emsp;本次开源的GREAT-FGO 1.0版本支持以下功能：

	1.支持基于因子图优化的RTK解算，可实现载波相位模糊度固定
	
	2.支持基于因子图优化的RTK/INS紧耦合解算，具备组合系统动态快速初始化能力
	
	3.支持GPS、GLONASS、Galileo、BDS-2/3等卫星导航系统

	4.支持自定义IMU数据格式、噪声模型
	
	5.支持轨迹动态显示与谷歌地图查看

	6.软件包还提供定位结果绘图脚本，便于用户对数据进行结果分析
	


## 软件包目录结构
```shell
GREAT-FGO_1.0
  ./src                     源代码 *
    ./app                  GREAT-PVTFGO、GREAT-GINSFGO、GREAT-MSF和GREAT-PVT主程序 *
    ./LibGREAT             因子图优化核心算法库 *
    ./LibGnut              Gnut库 *
    ./Third-party          第三方库 *
  ./sample_data          算例数据 *
  ./plot                 绘图工具 *
  ./doc                  GREAT-FGO相关文档 *
```

## 安装和使用

参见**doc**文件夹中的《GREAT-FGO说明文档 1.0.pdf》或关注我们团队后续在视频网站bilibili发布的讲解视频。



## 参与贡献

开发人员：

武汉大学GREAT团队, Wuhan University.

三方库：

* GREAT-FGO使用G-Nut库(http://www.pecny.cz)
  Copyright (C) 2011-2016 GOP - Geodetic Observatory Pecny, RIGTC.
  
* GREAT-FGO使用pugixml库(http://pugixml.org)
  Copyright (C) 2006-2014 Arseny Kapoulkine.

* GREAT-FGO使用Newmat库(http://www.robertnz.net/nm_intro.htm)
  Copyright (C) 2008: R B Davies.

* GREAT-FGO使用spdlog库(https://github.com/gabime/spdlog)
  Copyright(C) 2015-present, Gabi Melman & spdlog contributors.

* GREAT-FGO使用GLFW库(https://www.glfw.org)
  Copyright (C) 2002-2006 Marcus Geelnard, Copyright (C) 2006-2019 Camilla Löwy

* GREAT-FGO使用Eigen库(https://eigen.tuxfamily.org)
  Copyright (C) 2008-2011 Gael Guennebaud

* GREAT-FGO使用PSINS库(https://psins.org.cn)
  Copyright(c) 2015-2025 Gongmin Yan

* GREAT-FGO使用Ceres 库(http://ceres-solver.org)
  Copyright 2023 Google Inc.
  
## 下载地址

GitHub：https://github.com/GREAT-WHU/GREAT-FGO

## 其它

欢迎加入QQ群(1009827379)参与讨论与交流。

微信公众号：GREAT智能导航实验室，我们将持续推送团队成果。

bilibili账号：GREAT智能导航实验室，我们将持续发布软件讲解视频。
