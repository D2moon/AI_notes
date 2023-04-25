## 光栅化

## 采样
通过Fliter(低通滤波器也即做卷积)将原图片变模糊再进行采样，按照一个像素在三角形内部的比例获得不同的颜色。
## 走样与反走样

锯齿化，增加采样点进行抗锯齿MSAA(Multisample anti-aliasing)，缺点增大了计算量。

### 其他抗锯齿方法
FXAA(Fast Approximate AA)
TAA(Temporal AA)

### 类似过程超分辨率
解决采样不足的问题
DLSS(Deep Learning Super Sampling)通过深度学习补充原高分辨率图片
