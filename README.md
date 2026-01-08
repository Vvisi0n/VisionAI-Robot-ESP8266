# 视界 Vision AI 桌宠
# Vision AI Desktop Pet (ShiJie)

<p align="center">
  <img src="https://img.shields.io/badge/Platform-ESP8266-orange" alt="Platform">
  <img src="https://img.shields.io/badge/Framework-Arduino-blue" alt="Framework">
  <img src="https://img.shields.io/badge/Version-1.0-green" alt="Version">
  <img src="https://img.shields.io/badge/License-MIT-yellow" alt="License">
</p>

## 🚀 项目简介 | Project Introduction
patAI 是一款基于 ESP8266 开发的智能交互机器人项目，集成了丰富的面部表情动画、流畅的机械控制和直观的用户交互界面。该项目充分展现了嵌入式系统在智能交互设备领域的强大应用潜力。

patAI is an intelligent interactive robot project developed based on ESP8266, integrating rich facial expression animations, smooth mechanical control, and an intuitive user interaction interface. This project fully demonstrates the strong application potential of embedded systems in the field of intelligent interactive devices.

## ✨ 核心特性 | Core Features

### 🎭 智能表情系统 | Intelligent Expression System
- **15+种情感行为**: 好奇、思考、开心、生气、眩晕、困倦等  
  **15+ Emotional Behaviors**: Curiosity, thinking, joy, anger, dizziness, drowsiness, etc.
- **实时动画渲染**: 流畅的表情切换和动画效果  
  **Real-time Animation Rendering**: Smooth expression switching and animation effects
- **动态行为生成**: 基于随机算法的智能行为表现  
  **Dynamic Behavior Generation**: Intelligent behavior performance based on random algorithms

### 🎮 人性化交互 | Humanized Interaction
- **旋转编码器导航**: 精准的菜单控制体验  
  **Rotary Encoder Navigation**: Precise menu control experience
- **多功能按键**: 支持单击、双击、长按操作  
  **Multi-function Button**: Supports single-click, double-click, and long-press operations
- **两级菜单系统**: 主菜单 + 子菜单的完整交互架构  
  **Two-level Menu System**: Complete interaction architecture with main menu + submenus

### 🤖 机械控制系统 | Mechanical Control System
- **双舵机控制**: X轴和Y轴360度头部运动  
  **Dual Servo Control**: 360° head movement on X and Y axes
- **平滑移动算法**: 自然的机械运动效果  
  **Smooth Movement Algorithm**: Natural mechanical movement effects
- **多种行为模式**: 探索、跟踪、放松等智能行为  
  **Multiple Behavior Modes**: Intelligent behaviors such as exploration, tracking, and relaxation

### 🎨 图形界面 | Graphic Interface
- **OLED显示**: 128×64高分辨率显示  
  **OLED Display**: 128×64 high-resolution display
- **圆角UI设计**: 现代化的用户界面  
  **Rounded UI Design**: Modern user interface
- **流畅动画**: 菜单切换和表情变化的平滑过渡  
  **Smooth Animation**: Seamless transition for menu switching and expression changes

## 📋 硬件需求 | Hardware Requirements

### 主要组件 | Main Components
| 组件 | 规格 | 数量 | Component | Specification | Quantity |
|------|------|------|-----------|---------------|----------|
| ESP8266开发板 | NodeMCU/WeMos D1 Mini | 1 | ESP8266 Development Board | NodeMCU/WeMos D1 Mini | 1 |
| OLED显示屏 | 0.96寸 128×64 I2C | 1 | OLED Display | 0.96-inch 128×64 I2C | 1 |
| 舵机 | SG90/MG90 (180度) | 2 | Servo Motor | SG90/MG90 (180°) | 2 |
| 旋转编码器 | EC11型 | 1 | Rotary Encoder | EC11 Type | 1 |
| 按键 | 轻触开关 | 1 | Button | Tact Switch | 1 |

### 引脚连接 | Pin Connections
| ESP8266引脚 | 功能 | 连接模块 | ESP8266 Pin | Function | Connected Module |
|------------|------|----------|-------------|----------|------------------|
| GPIO4 (D2) | SDA | OLED显示屏 | GPIO4 (D2) | SDA | OLED Display |
| GPIO5 (D1) | SCL | OLED显示屏 | GPIO5 (D1) | SCL | OLED Display |
| GPIO15 (D8) | PWM | X轴舵机 | GPIO15 (D8) | PWM | X-axis Servo |
| GPIO12 (D6) | PWM | Y轴舵机 | GPIO12 (D6) | PWM | Y-axis Servo |
| GPIO13 (D7) | A相 | 旋转编码器 | GPIO13 (D7) | Phase A | Rotary Encoder |
| GPIO14 (D5) | B相 | 旋转编码器 | GPIO14 (D5) | Phase B | Rotary Encoder |
| GPIO0 (D3) | 按键 | 用户按键 | GPIO0 (D3) | Button | User Button |

## 🛠️ 软件架构 | Software Architecture

### 项目结构 | Project Structure
```
patAI/
├── patAI.ino          # 主程序入口 | Main program entry
├── Animation.h/cpp    # 动画和表情系统 | Animation and expression system
├── servo.h/cpp        # 舵机控制系统 | Servo control system
├── menu.h/cpp         # 用户界面系统 | User interface system
├── utils.h/cpp        # 工具函数和输入处理 | Utility functions and input processing
└── src/
    └── 位图资源.txt   # 图形资源文件 | Graphic resource file
```

### 核心模块 | Core Modules
- **Animation模块**: 处理所有图形显示和动画效果  
  **Animation Module**: Handles all graphic display and animation effects
- **Servo模块**: 控制舵机运动和智能行为  
  **Servo Module**: Controls servo movement and intelligent behaviors
- **Menu模块**: 管理用户界面和交互逻辑  
  **Menu Module**: Manages user interface and interaction logic
- **Utils模块**: 处理编码器和按键输入  
  **Utils Module**: Processes encoder and button input

## 📦 安装指南 | Installation Guide

### 1. 环境准备 | Environment Preparation
```bash
# 安装Arduino IDE | Install Arduino IDE
# 添加ESP8266开发板支持 | Add ESP8266 board support
# 安装所需库文件 | Install required libraries:
# - Adafruit GFX Library
# - Adafruit SSD1306
# - Servo Library
```

### 2. 硬件连接 | Hardware Connection
按照引脚连接表正确连接所有组件，注意电源供应要充足。  
Connect all components correctly according to the pin connection table, ensuring sufficient power supply.

### 3. 软件配置 | Software Configuration
```cpp
// 在patAI.ino中配置WiFi（可选） | Configure WiFi in patAI.ino (optional)
const char* ssid = "你的WiFi名称 | Your WiFi Name";
const char* password = "你的WiFi密码 | Your WiFi Password";
```

### 4. 编译上传 | Compilation and Upload
- 选择正确的ESP8266开发板 | Select the correct ESP8266 development board
- 设置正确的端口 | Set the correct port
- 编译并上传代码 | Compile and upload the code

## 🎯 使用说明 | Usage Instructions

### 基本操作 | Basic Operations
1. **旋转编码器**: 上下导航菜单 | **Rotary Encoder**: Navigate menus up and down
2. **单击按键**: 进入子菜单或确认选择 | **Single-click Button**: Enter submenu or confirm selection
3. **双击按键**: 返回上一级菜单 | **Double-click Button**: Return to the previous menu
4. **长按按键**: 特殊功能（可配置） | **Long-press Button**: Special functions (configurable)

### 功能演示 | Function Demonstration
- **表情展示**: 通过菜单选择不同的表情动画  
  **Expression Display**: Select different expression animations through the menu
- **头部运动**: 控制机器人头部进行各种动作  
  **Head Movement**: Control the robot's head to perform various movements
- **智能行为**: 观察机器人的自主行为表现  
  **Intelligent Behavior**: Observe the robot's autonomous behavior performance

## 🔧 开发指南 | Development Guide

### 添加新表情 | Add New Expressions
在`Animation.cpp`中添加新的表情函数 | Add a new expression function in `Animation.cpp`:
```cpp
void draw_new_expression() {
    // 实现新的表情绘制逻辑 | Implement new expression drawing logic
}
```

### 扩展行为模式 | Extend Behavior Modes
在`servo.cpp`的`random_behavior()`函数中添加新的行为模式。  
Add new behavior modes in the `random_behavior()` function of `servo.cpp`.

### 自定义菜单 | Customize Menus
修改`menu.cpp`中的菜单项配置来添加新功能。  
Modify the menu item configuration in `menu.cpp` to add new functions.

## 📊 技术规格 | Technical Specifications

### 性能指标 | Performance Metrics
- **编码器检测**: 5ms高精度检测间隔  
  **Encoder Detection**: 5ms high-precision detection interval
- **按键消抖**: 20ms稳定消抖算法  
  **Button Debouncing**: 20ms stable debouncing algorithm
- **动画帧率**: 流畅的60fps显示效果  
  **Animation Frame Rate**: Smooth 60fps display effect
- **舵机响应**: 实时平滑运动控制  
  **Servo Response**: Real-time smooth motion control

### 资源使用 | Resource Usage
- **程序空间**: ~80% (ESP8266 4MB Flash)  
  **Program Space**: ~80% (ESP8266 4MB Flash)
- **内存使用**: ~60% (ESP8266 80KB RAM)  
  **Memory Usage**: ~60% (ESP8266 80KB RAM)
- **功耗**: 待机模式 < 50mA，工作模式 < 200mA  
  **Power Consumption**: Standby mode < 50mA, Working mode < 200mA

## 🤝 贡献指南 | Contribution Guidelines

我们欢迎各种形式的贡献！请参考以下步骤 | We welcome contributions in all forms! Please follow these steps:

1. Fork本项目 | Fork this project
2. 创建功能分支 | Create feature branch (`git checkout -b feature/AmazingFeature`)
3. 提交更改 | Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 | Push to the branch (`git push origin feature/AmazingFeature`)
5. 开启Pull Request | Open a Pull Request

## 📝 更新日志 | Changelog

### v1.0 (当前版本 | Current Version)
- ✅ 基础表情动画系统 | Basic expression animation system
- ✅ 完整的机械控制系统 | Complete mechanical control system
- ✅ 流畅的用户交互界面 | Smooth user interaction interface
- ✅ WiFi连接框架 | WiFi connection framework
- ✅ 丰富的表情和行为库 | Rich expression and behavior library

## 🐛 故障排除 | Troubleshooting

### 常见问题 | Common Issues
1. **OLED不显示**: 检查I2C地址和接线  
   **OLED No Display**: Check I2C address and wiring
2. **舵机不运动**: 确认电源供应充足  
   **Servo Not Moving**: Ensure sufficient power supply
3. **编码器不响应**: 检查引脚连接和方向设置  
   **Encoder No Response**: Check pin connections and direction settings
4. **程序崩溃**: 检查内存使用和堆栈大小  
   **Program Crash**: Check memory usage and stack size

### 调试技巧 | Debugging Tips
启用串口调试输出查看详细运行信息 | Enable serial debug output to view detailed running information:
```cpp
Serial.begin(115200);
```

## 📄 许可证 | License

本项目采用MIT许可证 - 查看 [LICENSE](LICENSE) 文件了解详情。  
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 致谢 | Acknowledgements
- 感谢Arduino社区提供的丰富库资源  
  Thanks to the Arduino community for providing rich library resources
- 感谢ESP8266开发团队的技术支持  
  Thanks to the ESP8266 development team for technical support
- 感谢所有为本项目做出贡献的开发者  
  Thanks to all developers who contributed to this project

## 📞 联系我们 | Contact Us

如有问题或建议，请通过以下方式联系 | For questions or suggestions, please contact us through:

- **项目主页**: [GitHub Repository]
- **问题反馈**: [Issues Page]
- **讨论区**: [Discussions]

---

<p align="center">
  Made with ❤️ by patAI Development Team
</p>
