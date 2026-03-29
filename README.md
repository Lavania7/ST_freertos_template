# 模板说明 & 注意事项
此模板为BNGU战队进行嵌入式开发和调试的快速模板
对没错，你现在不需要花十几分钟新建工程了
尤其是那个C板的STM32F407IGHx……一堆引脚烦死了
还有烦人的keil……
不过现在，你不需要反复打开某蓝色和绿色软件了


> **更多内容，参考MDK-ARM文件夹下.Doc里的readme文件**


## 如何使用此模板开发
以下文件树展示了一个标准的战队级工程文件：
```shell
ROOT:.
│
├─ App      # 应用层（实例化与业务逻辑）
│   ├─ main.c
│   ├─ chassis_app.c
│   ├─ gimbal_app.c
│   └─ ...
│
├─ Bsp      # 板级支持包（硬件抽象）
│   ├─ bsp_gpio.c
│   ├─ bsp_uart.c
│   ├─ bsp_can.c
│   └─ ...
│
├─ Drv      # 驱动层（OOP: 类 + 方法 + 继承 + 多态）
│   ├─ motor.c
│   ├─ imu.c
│   ├─ encoder.c
│   └─ ...
│
├─ Lib      # 通用库（OOP: 工具类 / 算法类）
│   ├─ pid.c
│   ├─ filter.c
│   ├─ math_utils.c
│   └─ ...
│
└─ Drivers  # 芯片厂商提供的底层驱动 (HAL, CMSIS)
│   ├─ stm32f4xx_hal.c
│   ├─ stm32f4xx_it.c
│   └─ ...
```

关于面向对象（OOP），请参阅同文件夹下的《面向对象编程简述》
