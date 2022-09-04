
## 导论 
### 信号  
信号：是信息的载体，反映消息的物理量。
电信号：随时间而变化的电压或电流，记作$u=f(t) \qquad i=f(t)$  

信号的频谱  
- 将信号从时域变换到频域，通过傅里叶变换
- 频谱：将信号分解为正弦信号的集合，得到其正弦信号幅值和相位随角频率变化的分布图形
    - 幅度频谱
    - 相位频谱

![正弦](https://pic4.zhimg.com/80/v2-efd684a2bd1ad611c97b4ac95d1dc94a.jpg)  

![方波](https://pic4.zhimg.com/80/v2-bad26938f4924b487777a4e94899ae7c.jpg)  

![方波](https://pic4.zhimg.com/80/v2-99b46efb45d09f3d52ea812c4a432fdf.jpg)

周期信号：离散频谱
非周期信号：连续频谱

- 模拟信号 时间与幅值都是连续信号
- 数字信号 时间与幅值都是离散信号
- 模拟电路:对模拟量进行处理的电路，最基本的处理是对信号的放大  



### 信号的线性放大

$$x_0=Ax_1$$  

$x_1$是电路的输入信号，$x_0$是电路的输出信号，$A$是电路的增益(放大倍数)。其中，$A$为常数时，$x_0$与$x_1$呈线性关系。

>这里其实就是线性代数的模型，更抽象化A可以是一个矩阵或者用特征值来代替。

实现线性放大的条件  

- 信号线性放大的条件:$A$必须为常数
- 放大后输出能量大于输入能量的要求
    - 放大电路需要能量供给
    - $|A| \gt 1$ ,且保持常数



放大电路的失真问题  

- 非线性失真
    - 放大电路输出有限导致的失真
    - 非线性器件导致的失真
- 非线性失真系数：$$\gamma=\frac{\sqrt{\sum_{k=2}^{\infty}X_{0k}^2}}{X_{ol}} \times 100\%$$
    - $X_{ol}$是输出信号基波分量的有效值，$X_{ok}$是各高次谐波分量的有效值，$k$为正整数。
    - 衡量放大电路的非线性失真程度
![非线性失真](https://pic4.zhimg.com/80/v2-5e3ed0b70a74dd4d6665c00e9edd54ea.jpg)

- 线性失真(频率失真)
    - 由于放大电路对不同频率分量产生不同的放大倍数和时延导致的失真
    - 频率失真包括幅度失真和相位失真

![线性失真](https://pic4.zhimg.com/80/v2-5da92be71631015d244b6abfce766e85.jpg)

![线性失真](https://pic4.zhimg.com/80/v2-4793c068c860ed97092a83f26d54fbcd.jpg)

频率失真与非线性失真的本质区别:频率失真不会产生输入信号中没有的新频率分量。  
减小频率失真的策略:要求放大电路对信号频带内所有频率分量的放大能力保持一致。  

![策略](https://pic4.zhimg.com/80/v2-fde1b4de397a5887d44dcde7641323ab.jpg)

### 放大电路模型  
- 一般构成
    - 需要供电电源
    - 是双口网络

![一般构成](https://pic4.zhimg.com/80/v2-d2029da6d8e0357666f033c17b307160.jpg)

放大电路的增益形式  

![增益形式](https://pic4.zhimg.com/80/v2-0bf28c4dd666a18c8ea5e2f7647ffecf.jpg)

![模型](https://pic4.zhimg.com/80/v2-302dc03cc117598015887d16f76693e3.jpg)
![模型](https://pic4.zhimg.com/80/v2-7dde68c8b3eb52c8ecfd135b3140d3f9.jpg)
![模型](https://pic4.zhimg.com/80/v2-20ff2502149c06ecdbe91c7cb193c471.jpg)
>没有星号标注的是比较重要的


## 理想运算放大器  

![学堂在线](https://pic4.zhimg.com/80/v2-697cd5c640332f81ac45cc57420216ff.jpg)
![学堂在线](https://pic4.zhimg.com/80/v2-2b1c5d8c4ca5099f496fcd95b7ba7919.jpg)
![学堂在线](https://pic4.zhimg.com/80/v2-f61d0cb4f0a50de5d9832d09869fa13e.jpg)

### 运算放大器的外接端子  
电路符号  
![电路符号](https://pic4.zhimg.com/80/v2-1ef8ab0cd88f6ad8ed9ac4817ab00d0f.jpg)

外接电源连接
![外接电源](https://pic4.zhimg.com/80/v2-f0fc964200b01cb5b55735fae30e7ba8.jpg)

### 运算放大器的传输特性  

- 运算放大器的输出电压和输入电压之间的关系曲线称为电压传输特性
    - 线性区:对输入信号进行线性放大
    - 饱和区:输入信号和输出信号不是线性放大关系

![传输特性](https://pic4.zhimg.com/80/v2-8c2b47cabeb18a8710635b5124299cbd.jpg)
### 理想运放特性  
- 理想运算放大器具有的参数
    - 开环电压增益$A_{vo} \rightarrow \infty$
    - 输入电阻$r_1=\infty$
    - 输出电阻$r_0=0$
    - 开环带宽$BW \rightarrow \infty$
    - 当$v_p=v_n$时，$v_o=0$

![参数](https://pic4.zhimg.com/80/v2-d8076d8d2bba0e3340f060701d6aa600.jpg)

![理想](https://pic4.zhimg.com/80/v2-cfc316074d722aa4fa0a09476978cfe8.jpg)
- 虚短和虚断，对于工作在线性区的理想运放，有两条重要法则:
    - 虚短:$v_P \approx v_N$(有交流负反馈)
    - 虚断:$i_i=\frac{v_{id}}{r_i} \approx 0$  
- 在非线性区则没有以上两个法则  



__例题:__  

![例题](https://pic4.zhimg.com/80/v2-c61f86a222c192d353598bed6672dfb5.jpg)
![例题](https://pic4.zhimg.com/80/v2-d3d6081cb57f15ceb60eb50e869c4091.jpg)
![例题](https://pic4.zhimg.com/80/v2-22e023bf174dcec48bf105ef50e85d61.jpg)

## 运放构成的基本电路

### 同相放大电路  
- 电路形式  

![电路形式](https://pic4.zhimg.com/80/v2-ef5496f963e590012fed95f7f2180e0f.jpg)
![电压增益](https://pic4.zhimg.com/80/v2-4235562888154e1544d08daa62fcac5b.jpg)
- 电路特点
    - 闭环电压增益$A_v \ge 1$,输出电压与输入电压同相位
    - 开环电压增益$A_{\infty} \rightarrow \infty$,但闭环电压增益$A_v$仅与外部电阻$R_l$与$R_f$有关(和运放本身的放大能力无关)
    - 输入电阻大，输出电阻小，带负载能力强



![应用](https://pic4.zhimg.com/80/v2-e2d601cbd937059a6098b40bcbaa25fd.jpg)
![优点](https://pic4.zhimg.com/80/v2-7d42c9f0db2cfaeecba152d2dc412188.jpg)

### 反相放大电路  
- 电路形式
![电路形式](https://pic4.zhimg.com/80/v2-5024918d30095f33f7b3effe0ab74111.jpg)
![电压增益](https://pic4.zhimg.com/80/v2-c4a9b6e47b043c23ace109b05a9ed30b.jpg)
- 电路特点
    - 闭环电压增益$A_v \le 0$,输出电压与输入电压反相
    - 闭环电压增益$A_v$仅与外部电阻$R_l$和$R_f$的值有关
    - 反相输入端是"虚地"
    - 输入电阻远小于同相放大电路的输入电阻



 