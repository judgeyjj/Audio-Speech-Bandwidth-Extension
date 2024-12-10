#  Notes of Speech and Audio

1. 听觉的掩蔽效应

   https://blog.csdn.net/kwenzhang1/article/details/142552558

   作用：让编解码器中过程中产生的量化失真低于掩蔽阈值，这样这些失真人耳就感知不到了。

2. 语谱图

   顺序：分帧加窗->短时傅里叶变换->频谱图逆时针旋转90°并对幅度值进行映射，通过量化的方式，0表示白，255表示黑色。幅度值越大，相应的区域越黑， 从而去除了幅度值，这个维度， 多出一个维度用作表达其他信息->时间作横轴，频率作纵轴形成语谱图。

   参考链接：https://blog.csdn.net/chumingqian/article/details/123019808

   https://blog.csdn.net/qq_36002089/article/details/108378796

3. 梅尔谱图

   语谱图往往是很大的一张图，为了得到合适大小的声音特征，往往把它通过梅尔标度滤波器组（mel-scale filter banks），变换为梅尔频谱。
   人耳听到的声音高低和实际（Hz）频率不呈线性关系，用Mel频率更符合人耳的听觉特性（这正是用Mel声谱图的一个动机，由人耳听力系统启发），即在1000Hz以下呈线性分布，1000Hz以上呈对数增长，Mel频率与Hz频率的关系为：
   fmel=2595⋅lg(1+f/700Hz)。
   有另一种计算方式为fmel=1125⋅ln(1+f700Hz)。

4. 倒谱

   频谱平方->功率谱->对数运算->逆傅里叶变换->倒谱

   上述步骤如果没有对数运算，可以得到自相关序列

​	参考链接：https://www.cnblogs.com/dream-and-truth/p/10655758.html