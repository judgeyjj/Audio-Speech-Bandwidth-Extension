#  Notes of Speech and Audio

1. 听觉的掩蔽效应

   https://blog.csdn.net/kwenzhang1/article/details/142552558

   作用：让编解码器中过程中产生的量化失真低于掩蔽阈值，这样这些失真人耳就感知不到了。

2. 语谱图

   顺序：分帧加窗->短时傅里叶变换->频谱图逆时针旋转90°并对幅度值进行映射，通过量化的方式，0表示白，255表示黑色。幅度值越大，相应的区域越黑， 从而去除了幅度值，这个维度， 多出一个维度用作表达其他信息->时间作横轴，频率作纵轴形成语谱图。

   参考链接：https://blog.csdn.net/chumingqian/article/details/123019808

   https://blog.csdn.net/qq_36002089/article/details/108378796

   