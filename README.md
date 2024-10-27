
## 前言


昨晚用 Protues 搭建了 51 的最小系统电路，在实物中好用的复位电路，到仿真里不能正常复位了。


51 单片机是高电平复位，所以在运行时 RST 引脚应该是低电平，但在仿真中 RST 引脚一直保持高电平，导致按下按键也不能复位单片机。


[![RST 引脚一直处于高电平](https://img2024.cnblogs.com/blog/2881477/202410/2881477-20241026112630033-1454165559.png)](https://github.com)


## 解决方法


我在网上搜索的解决方法一共有两种：


### 1、改电阻的阻值


将复位电路的电阻改为 100Ω


[![100Ω 时运行](https://img2024.cnblogs.com/blog/2881477/202410/2881477-20241026112630178-37718441.png)](https://github.com)


### 2、改电阻的属性


双击复位电路的电阻，找到 Model Type ，下拉选择 DIGITAL


[![设置电阻属性](https://img2024.cnblogs.com/blog/2881477/202410/2881477-20241026112630582-1556425716.png)](https://github.com)


[![设置为 DIGITAL 时运行](https://img2024.cnblogs.com/blog/2881477/202410/2881477-20241026112630152-1791524025.png)](https://github.com):[蓝猫机场](https://fenfang.org)


## 后记


经过测试设置一个或两个都设置，单片机均可以正常复位。


参考链接：


[https://zhidao.baidu.com/question/513862596\.html](https://github.com)


[https://zhidao.baidu.com/question/335752137\.html](https://github.com)


