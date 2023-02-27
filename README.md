# LAN9514-USBtools
多功能USB调试工具，提供USB转以太网、RS485、RS422、TTL * 2、USB 2.0 HUB * 2。使用type-C或type-B连接，USB供电不足时可使用DC电源供电。

## 实物图
![正面](https://github.com/xxxlzjxxx/LAN9514-USBtools/PICTURE/实物图.png)

![正面](https://github.com/xxxlzjxxx/LAN9514-USBtools/PICTURE/顶层.png)
![背面](https://github.com/xxxlzjxxx/LAN9514-USBtools/PICTURE/底层.png)

### 使用说明
1. 安装USB转串口芯片驱动。根据操作系统下载对应的驱动程序：[CP210x USB to UART Bridge VCP Drivers](https://www.silabs.com/developers/usb-to-uart-bridge-vcp-drivers?tab=downloads)。
2. 使用USB type B或C插头连接PCB。J
![驱动安装成功图示](https://github.com/xxxlzjxxx/LAN9514-USBtools/PICTURE/设备管理器.png)
3. 设备管理器中所示Enhanced COM Port和Standard COM Port与PCB上丝印所示一一对应。其中Standard COM Port提供TTL电平的串口通信排针与DB9公头插座的232电平的串口通信插座。Enhanced COM Port提供RS485通信插座。LAN9512/LAN9514 USB 2.0 to Ethernet 10/100 Adapter为标准百兆以太网接口。同时PCB提供3个USB2.0速率的接口。
4. 通用串行总线interface features：

|  Standard COM Port   |   |
| ------- | --- |
|  数据格式  |  8位数据位，1位停止位 |
|   校验   |  奇、偶、无校验 |
|  波特率  |  2400 bps - 921600 bps |
|   缓冲大小   |  288 Byte |   

|  Enhanced COM Port   |   |
| ------- | --- |
|  数据格式  |  5、6、7、8位数据位，1、1.5、2位停止位 |
|   校验   |  奇、偶、标记、空格、无校验 |
|  波特率  |  300bps - 2Mbps |
|   缓冲大小   |  320 Byte |

5. **_备注_** 。如果外设功耗过高，需要对DC插座供电。DC电源输入电压范围为5V-12V。
