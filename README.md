# WCSPH · Interactive Lecture

**WCSPH：由密度误差驱动的显式压力反馈**

[在线阅读交互讲义](https://heytau.github.io/wcsph-lecture-interactive/) · [下载完整源码](wcsph-lecture-interactive-source.zip)

独立的交互阅读版本，包含完整中文讲义、38 个独立公式、162 处行内公式与 7 张矢量插图。

- **粒子与密度**：调整粒子间距、平滑长度，观察一维核密度重建。
- **Tait 状态方程**：调整人工声速、非线性指数和密度偏差，对照压力与线性近似。
- **时间步限制**：比较声学、加速度、黏性和表面张力给出的时间步上限。
- 章节导航、阅读进度和可放大的矢量插图。

## 使用

`index.html` 是完整的独立网页。直接下载并用浏览器打开即可离线使用，字体、图片和交互代码均已内嵌，无需网络、插件或登录。

## 修改与重建

下载并解压 `wcsph-lecture-interactive-source.zip`。需要 Node.js 22 或更新版本：

```sh
npm ci
npm run build
npm run check
npm run preview
```

原稿为 `lecture.md`，样式与交互组件位于 `src/`，构建后的目录式网站位于 `docs/`。执行 `npm run standalone` 可以重新生成独立 HTML。

## 模型说明

密度实验使用归一化的一维 cubic spline 核，粒子质量为 0.2 kg，显示线密度 kg/m。Tait 实验展示未截断压力；时间步实验中的安全系数是教学示例，不能替代具体离散方法的稳定性验证。学术引用保留在讲义末尾的 `Reference:` 中。

使用 [KaTeX](https://katex.org/) 与 [markdown-it](https://github.com/markdown-it/markdown-it)。第三方许可证收录在源码压缩包中。本仓库未授予讲义和插图额外的开放许可。

