# ESP32-C3-Clock
项目简介 / Project Introduction
中文版本
这是一个基于ESP32的赛博朋克风格智能网络时钟，集成了多种先进功能，支持STA模式（客户端模式）和AP模式（热点模式）的双重工作模式：
双模式工作机制：
STA模式（时钟模式）：设备连接到已配置的WiFi网络，作为客户端正常工作时钟，同步NTP时间，显示温湿度、电池电量等信息
AP模式（配置模式）：设备作为热点（SSID: “Clock”），提供Web配置界面，用于添加/管理WiFi网络和设置参数
核心功能：
智能网络切换：STA模式下自动在已保存的5个WiFi网络中切换，优先连接信号最强的网络
故障自动恢复：STA模式连接失败或时间同步失败时自动重启，保障系统稳定运行
精准时间同步：双NTP服务器冗余设计，主备服务器自动切换
环境智能感知：SHT31传感器提供精准温湿度数据，用于电池温度补偿算法
双模式电量管理：STA/AP模式分别使用优化的ADC校准参数，确保电量测量准确性
实时状态显示：雷达扫描动画、电池进度条、温湿度数字显示一体化界面
便捷配置：通过AP模式的Web界面轻松管理WiFi网络和时区设置
智能节能：触摸进入深度睡眠，再触摸唤醒，延长电池续航
技术特色:
STA模式界面灵感：时钟主界面设计灵感来源于 YouTube 创作者 Huy Vector 的赛博朋克风格作品
智能网络优先级：STA模式下自动扫描并选择RSSI最强的已保存网络
温度补偿算法：利用SHT31温度数据对电池电压进行精准补偿
双重电池校准：STA模式和AP模式使用独立的ADC转换因子和分压比参数
时间同步保障：15分钟定期同步，失败自动重启，确保时间准确性
中文字符处理：自动过滤SSID中的非ASCII字符，确保显示稳定性
多种交互方式：双击进入电池测试，长按重启，单击切换配置页面
硬件配置：
主控：ESP32-C3
屏幕：0.96英寸TFT显示屏（160x80分辨率）
传感器：SHT31温湿度传感器（I2C接口）
电池：18650锂电池，带分压电路测量
交互：GPIO1电容触摸按键
引脚配置：SDA(GPIO2), SCL(GPIO0), TFT屏幕使用专用SPI引脚
这是一个功能完善、界面炫酷的智能时钟项目，完美融合了物联网连接、环境感知和用户交互，适合作为桌面智能终端或物联网开发学习平台。
材料清单和重要提示在[这里](https://github.com/AndYou-a/ESP32-C3-Clock/blob/4e75d7cc0e85aebd8d4fcb729db71a940c304edb/list.notes)
源码和固件下载在[Releases](https://github.com/AndYou-a/ESP32-C3-Clock/releases)界面

===========================================================================================================================================

English Version
This is a cyberpunk-style smart network clock based on ESP32, integrating multiple advanced features with dual STA mode (client mode) and AP mode (access point mode) operation:
Dual-Mode Operation Mechanism:
STA Mode (Clock Mode): Device connects to configured WiFi networks as a client, functioning as a normal clock with NTP time synchronization, displaying temperature/humidity, battery level, etc.
AP Mode (Configuration Mode): Device acts as a hotspot (SSID: “Clock”), providing a web interface for adding/managing WiFi networks and configuring parameters
Core Features:
Smart Network Switching: In STA mode, automatically switches between up to 5 saved WiFi networks, prioritizing the strongest signal
Automatic Fault Recovery: Auto-reboots when STA mode connection fails or time synchronization fails, ensuring system stability
Precise Time Synchronization: Redundant dual NTP server design with automatic failover
Environmental Intelligence: SHT31 sensor provides accurate temperature/humidity data for battery temperature compensation algorithm
Dual-Mode Battery Management: STA/AP modes use optimized ADC calibration parameters for accurate battery measurement
Real-time Status Display: Integrated interface with radar sweep animation, battery progress bar, and temperature/humidity digital display
Easy Configuration: Web-based interface in AP mode for easy WiFi network and timezone management
Smart Power Saving: Touch to enter deep sleep, touch again to wake up, extending battery life
Technical Highlights:
STA Mode Interface Inspiration: Clock main interface design inspired by cyberpunk-style works from YouTube creator Huy Vector
Smart Network Prioritization: In STA mode, automatically scans and selects saved network with highest RSSI
Temperature Compensation Algorithm: Uses SHT31 temperature data for precise battery voltage compensation
Dual Battery Calibration: Separate ADC conversion factors and voltage divider ratios for STA and AP modes
Time Sync Guarantee: 15-minute periodic synchronization with auto-reboot on failure, ensuring time accuracy
Chinese Character Handling: Automatic filtering of non-ASCII characters in SSID for stable display
Multiple Interaction Methods: Double-click for battery test, long press for reboot, single click for configuration page switching
Hardware Configuration:
MCU: ESP32-C3
Display: 0.96-inch TFT screen (160x80 resolution)
Sensor: SHT31 temperature & humidity sensor (I2C interface)
Battery: 18650 lithium battery with voltage divider circuit measurement
Interaction: GPIO1 capacitive touch button
Pin Configuration: SDA(GPIO2), SCL(GPIO0), TFT screen uses dedicated SPI pins
This is a fully-featured, visually stunning smart clock project that perfectly integrates IoT connectivity, environmental sensing, and user interaction. Ideal as a desktop smart terminal or IoT development learning platform.
[Materials List And Important Notes](https://github.com/AndYou-a/ESP32-C3-Clock/blob/4e75d7cc0e85aebd8d4fcb729db71a940c304edb/list.notes)
Download firmware and code from [Releases](https://github.com/AndYou-a/ESP32-C3-Clock/releases)
![80097824b85e2bf1d27417dcf0d11cbe](https://github.com/user-attachments/assets/aa057a57-5442-4322-8433-60b31920f7bc)
![c8c0215cec37bcd124b51ea81b5bafdb](https://github.com/user-attachments/assets/bb3ee20e-279f-45a3-bb19-ca75a43812e4)
![47c000e698bfd3ea7fcf0f7873494151](https://github.com/user-attachments/assets/c1c2ace1-83f1-4f06-9670-ee31365de00a)
![eee7815d4c2d6e730fa84b29f42587a0](https://github.com/user-attachments/assets/633d2775-11d7-43c3-82c1-4751161e88da)
