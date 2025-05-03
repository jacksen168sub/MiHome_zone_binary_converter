# 米家智能家居人在传感器区段二进制转换器

![MiHome_zone_binary_converter](https://github.com/jacksen168sub/MiHome_zone_binary_converter/blob/main/images/main.png)

## MiHome_zone_binary_converter/Mi Home Zone Binary Converter/Mi Smart Home Human Presence Sensor Zone Binary Converter

demo地址: [在线预览](https://mihome-zone-binary-converter.netlify.app)

## 介绍
一个用于应对米家传感器(目前而言就领普人体存在传感器ES3)在Xiaomi中枢网关极客版中 ```BLE专用自定义服务(ble专用，事件参数总长度不能超过9字节近距区间无人0有人1-255)``` 的2进制转10进制的转换器(web页面)。

![1](https://github.com/jacksen168sub/MiHome_zone_binary_converter/blob/main/images/1.png)

![2](https://github.com/jacksen168sub/MiHome_zone_binary_converter/blob/main/images/2.png)


## 目前已发现采用2进制的米家设备:
1. 领普人体存在传感器ES3


### 关于领普人体传感器ES3的发现:
在米家APP内设置了 ```自定义近距区间``` 会控制在米家自动化极客版内的查询结果:
![3](https://github.com/jacksen168sub/MiHome_zone_binary_converter/blob/main/images/3.png)
如图设置了 ```2.25米内``` 换算成10进制值就是: **1-7**
![4](https://github.com/jacksen168sub/MiHome_zone_binary_converter/blob/main/images/4.png)
![5](https://github.com/jacksen168sub/MiHome_zone_binary_converter/blob/main/images/5.png)

那么在米家自动化极客版内查询的值就会被控制在**7**之内,不会超过**7**

假设传感器显示8个格子能量值全满了(11111111 = 255),那么在米家自动化极客版内的查询结果就会是**7**,而不会是**8-255**