# Arduino


## 1. Arduino简介  

Arduino是一种开源电子原型平台，受到开发者和爱好者的广泛欢迎。它由硬件和软件组成，硬件包括多种开发板，如Arduino UNO、MEGA等，软件主要是Arduino IDE，用于编写和上传代码到开发板上。Arduino适用于许多项目，包括机器人、传感器控制和物联网应用。由于其简单易用的特性和庞大的社区支持，Arduino是学习编程和电子学的理想选择。  

## 2. 接线图  

![](media/3b93afbcf6a53aaac1b35355b85ef9fb.png)  

## 3. 测试代码（测试软件版本：arduino-1.8.12）  

```cpp  
void setup(){  
    pinMode(2, OUTPUT); // 数字口2设置为输出  
    pinMode(3, OUTPUT); // 数字口3设置为输出  
}  

void loop(){  
    //设置风扇逆时针转3000毫秒  
    digitalWrite(2, LOW);  
    digitalWrite(3, HIGH);  
    delay(3000);  

    //设置风扇停止转动1000毫秒  
    digitalWrite(2, LOW);  
    digitalWrite(3, LOW);  
    delay(1000);  

    //设置风扇顺时针转3000毫秒  
    digitalWrite(2, HIGH);  
    digitalWrite(3, LOW);  
    delay(3000);  
}  
```  

## 4. 代码说明  

将管脚设置为2、3。当3输出为高电平，2输出为低电平时，电机逆时针旋转；当3和2都设置为低电平时，电机停止转动。当3输出为低电平时，2输出为高电平时，电机顺时针旋转；

## 5. 测试结果  

在控制板上上传成功，按照接线图接线，拨码开关拨打到右端上电后，小风扇先逆时针转3000毫秒，停止1000毫秒，再顺时针转3000毫秒，小风扇以较快的速度运转。



