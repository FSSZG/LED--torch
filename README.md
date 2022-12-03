# LED恒流驱动手电筒

##### 此项目的LED手电筒+移动电源功能设计由纯硬件实现   SW6106负责为电池充电和为TYPE-C口提供快充输入输出的功能  大功率LED恒流驱动电源由SW6106的另一路输出接口通过CH224K诱骗12V1.5A 18W输出得来 再由LM358运放经分流电阻采样电压和参考电压比较控制NMOS开关实现硬件可调恒流的功能 

##### 由于大功率LED工作起来发热十分严重普通的被动散热已经无法满足需求 所以此项目采用主动风冷散热 通过NTC热敏电阻实时采集散热片温度 由LM358运放构建的迟滞比较器 来控制 风扇电源开关 来控制LED散热片温度

#### 功能参数
1. 电池由两节18650并联  4A 高效率开关充电  18W 高效同步升压输出（同一时间只能处于一种工作模式）
2. Type-C 支持 PD3.0/PD2.0/QC3.0/QC2.0/FCP/PE2.0/PE1.1/SFCP 快充输出，支持 PD3.0/PD2.0 快充输入
3. 一路大功率LED恒流驱动（最大12V 1.5A 18W）   一路小功率LED恒流驱动   4个LED 灯电量指示 和1个快充LED指示灯
4.  1个控制大功率LED按键（长按按键打开和关闭输出） 一个拨盘电位器 （控制LED亮度） 1个控制小功率LED按键（按下亮 不按灭）
5.  12V 2006(20*20*6.2mm) 风扇驱动  NTC温度>40°左右开启风扇   NTC温度<30°左右关闭风扇
6.  待机功耗40uA左右 6000mAh 锂电池满电情况下 12W LED 功率全开  续航大概100分钟左右  
 
#### 器件信息
1.  最终成品主要由： 外壳 + PCBA + 两节18650电池 + LED灯板 + 聚光透镜 + 散热片 + 2006风扇 + 点状激光头 + M2铜柱和平头螺丝组成
2.  成品外壳长宽高：120*49*25mm  分别由外壳1和头套1组成  通过4颗M2*5平头螺丝固定     由在嘉立创3D打印生产
3.  PCBA ：双层板 1.6板厚 由两块独立PCBA组成 通过4根M2*4双通铜柱 和 8颗M2*3平头螺丝连接在一起（注意方向）
4.  18650 锂电池默认使用普通4.2V电压的   如需使用高压锂电池 需要更改SW6106相关配置电阻  容量越高续航越长
5.  LED灯板由灯珠和散热基板组成 灯板宽度<19mm 灯芯高度<1mm  灯珠必须使用平头封装否则无法安装聚光透镜  只要尺寸参数合适任意灯珠都能使用
6.  聚光透镜由于 头套1 的结构设计只能使用直径12*高6mm的无边透镜  尽量选用玻璃材质
7.  散热片由于结构设计只能使用 22*22*20mm 的散热器  LED灯板可通过导热硅胶 导热双面胶等方法固定到散热片上   安装时有方向要求
8.  2006散热风扇长宽高：20*20*6.2mm 尺寸可以小不能大  12V供电   安装时最先安装散热风扇 导线要经外壳卡口引出
9.  激光头尺寸：直径12mm  高<20mm   输出：3V~4.2V  最大恒流160mA供电  颜色任意 不一定要用激光头 也可以驱动其他小功率LED 

#### 购买参考
1. LED灯板 我使用的是从投影灯上拆机的 好像是 XHP50D灯珠 网上没看的一样的 购买注意灯珠电压功率封装和基板尺寸  参数合适任意灯珠都能使用
2. 聚光透镜：https://m.tb.cn/h.URlB8qP?tk=PnWUddMsYJw
3. 散热片：https://m.tb.cn/h.URlBhLm?tk=c3MbddMIdLp
4. 散热风扇 ：https://m.tb.cn/h.URlB3RJ?tk=W1FuddMIzUn
 
#### 注意事项
1. 电池充电时和为其他设备充电时   大功率LED无法使用  将自动熄灭 
2.  装配时先把 头套部分装好在把导线焊在PCBA上在进行最终组装    3D打印外壳材质尽量选用耐高温的 
3.  PCB板厚1.6mm   元件参数以原理图参数为准   部分元件参数需根据使用的器件重新计算  硬件资料和外壳设计资料在附件内 
4.  此项目比较复杂 新手不建议自制   相较演示图片中的作品 开源的设计都经过部分优化改进 

#### 装配演示
![输入图片说明](img/1%20(1).jpg)
![输入图片说明](img/2%20(1).jpg)
![输入图片说明](img/3%20(1).jpg)
![输入图片说明](img/4%20(1).jpg)
![输入图片说明](img/5%20(1).jpg)
![输入图片说明](img/6%20(1).jpg)
![输入图片说明](img/7%20(1).jpg)
![输入图片说明](img/8%20(1).jpg)
![输入图片说明](img/9%20(1).jpg)