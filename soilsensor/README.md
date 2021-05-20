# Soil moisture sensor

## model: 

![img](https://raw.githubusercontent.com/zhuhu00/img/master/20210520125944.jpeg)

Link：[taobao](https://item.taobao.com/item.htm?scm=1007.13982.82927.0&id=577950984281&last_time=1621307623)

## Usage

Connecting circuit as following:

![img](https://raw.githubusercontent.com/zhuhu00/img/master/20210520130651.jpeg)

We use Raspberry pie to receive data from the soil moisture sensor. It has following pins:

![img](https://raw.githubusercontent.com/zhuhu00/img/master/20210520130907.png)

then, we connect like this:

![树莓派土壤湿度传感器](https://raw.githubusercontent.com/zhuhu00/img/master/20210520131310.jpeg)

After this, the power indicator will light(in our model is red): 

![o4YBAFplRKeAdHGgAAA7jS9azmU334](https://raw.githubusercontent.com/zhuhu00/img/master/20210520131241.jpg)

Finally, use the following code to get data:

```python
#!/usr/bin/python
# -*- coding: UTF-8 -*-
import RPi.GPIO as GPIO
import time

channel = 21 #管脚40，参阅树莓派引脚图，物理引脚40对应的BCM编码为21

GPIO.setmode(GPIO.BCM)
GPIO.setup(channel, GPIO.IN)

while True:
        if GPIO.input(channel) == GPIO.LOW:
                print "土壤检测结果：潮湿"
        else:
                print "土壤检测结果：干燥"
        time.sleep(1)
```

