一、工程配置笔记：

芯片型号：STM32F103C8T6

系统时钟：配置为72MHz

开发环境：Makefile+ARM GCC+Vscode

烧录工具：STM32CubeProgrammer+ST-link

二、引脚配置：

PA13 -> SYS_JIMS-SWDIO -> ST-Link调试数据线

PA14 -> SYS_JTCK-SWCLK -> ST-Link调试时钟线

PA10 -> USART1_RX -> 单片机接收端

PA9 -> USART1_TX -> 单片机发送端

PA5 -> ADC1_IN5 -> adc读取电位器的电压值

PA6 -> TIM3_CH1 -> 与舵机相连控制舵机角度

PB6 -> TIM4_CH1 -> 与led相连控制呼吸灯

其余引脚不接线不列出

三、编译与烧录：

编译：终端输入make

连接ST-Link与板子

烧录：终端输入make flash

工程配置如下
![alt text](05project.png)

呼吸灯，串口发送角度舵机旋转和电位器adc的演示见附件
https://github.com/Happy-19/LightChaser-Training-62/releases/download/v1.0/05_pwm_adc.mp4