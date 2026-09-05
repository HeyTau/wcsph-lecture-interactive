# WCSPH Explainer

[在线探索与阅读](https://heytau.github.io/wcsph-lecture-interactive/)

拖动一个粒子，追踪「位置 → 核权重 → 密度 → 压力 → 显式推进」。点击计算阶段查看对应局部计算，点选贡献项与粒子位置对照，播放或单步执行真实的 SPH 更新。页面与矢量插图采用统一的浅色底面。

讲义原文、38 个编号公式、7 张矢量图、字体和交互代码全部包含在 index.html 中，下载后可离线打开。

## 可编辑源码

下载并解压 [完整源码 ZIP](./wcsph-lecture-interactive-source.zip)，使用 Node.js 22 或更新版本执行 npm ci、npm run build、npm run check。npm run standalone 生成独立 HTML。

## 模型范围

121 个等质量粒子，二维单位厚度切片，密度单位 kg/m³。二维 cubic spline 核、Tait 状态方程、非负压力、对称压力力及半隐式 Euler；时间步由当前场自适应计算。关闭重力与表面张力，边缘邻域不作密度补偿，可选对称耗散黏性。页面的「模型与单位」提供详细说明。

## Reference

交互组织参考 [CNN Explainer](https://github.com/poloclub/cnn-explainer)，未使用其代码或图像。物理内容与引用见原讲义及源码 README。此前版本保留在 Git 历史中。
## 新增交互组件

- [离散粒子如何表示连续场](https://heytau.github.io/wcsph-lecture-interactive/#lab-reconstruction)：拖动采样点、调节核宽、追踪单个粒子贡献，比较原始求和与归一化重建。
- [随体导数](https://heytau.github.io/wcsph-lecture-interactive/#lab-material)：比较固定测点与移动粒子的温度历史，实时分解局部项、对流项和随体导数，支持播放、回看与单步。

两组件随原稿嵌入第 1.3 节与第 2.1 节之后。详细模型见页面说明和源码 README。
