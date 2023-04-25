## Shading(着色)

### Z-Buffer算法

解决不同三角形之间覆盖的问题，存储每个像素的深度，保留最小深度的颜色。



### Shading

为不同的物体赋予不同的材质，只考虑这一点的光照，不考虑阴影。

![image-20230316164943242](C:\Users\Dreamoon\AppData\Roaming\Typora\typora-user-images\image-20230316164943242.png)

### 漫反射

光线和法线角度导致仅吸收部分光源，反射光呈球形发射，能量与到反射点的距离的平方成反比。

![image-20230316170200536](C:\Users\Dreamoon\AppData\Roaming\Typora\typora-user-images\image-20230316170200536.png)