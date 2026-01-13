
还需要准备什么？
===============================

在开始使用本套件之前，我们需要先准备一些必要的硬件。

必备组件
------------------------------

* **Raspberry Pi**

  Raspberry Pi 充当整个系统的 **大脑**，负责所有的计算、传感和控制任务。  
  
  .. image:: /_shared/pi_start/img/need_pi.jpg

  * **兼容型号**：Raspberry Pi 5、Raspberry Pi 4、3 或 Raspberry Pi Zero 2W  
  * **最低配置**： **2GB 内存** —— 足以运行所有标准 Python 项目，以及使用 **在线 AI 服务**，如 OpenAI Whisper、TTS 或 LLM。  
  * **推荐配置**： **4GB 或更高内存** —— 在同时运行 **本地 AI 模型** （如 Vosk 语音识别、Piper TTS 或轻量级 LLM）、摄像头视频流和控制任务时，可获得更流畅的性能。  
  

* **电源适配器**

  本套件配备了 **18650 电池盒** 和带有内置充电电路的 **Fusion HAT+** 扩展板。
  
  .. image:: /_shared/pi_start/img/need_power.png
    :width: 400

  * 充电时，建议使用 **5V 3A 电源适配器**，例如官方的 **Raspberry Pi 15W USB-C 电源**。  
  * 也可以使用 **USB-C Power Delivery（PD）充电器** 或 **QC 2.0 快充充电器**。  
  * 从 0% 充至 100% 通常需要大约 **2 小时**。  


* **Micro SD 卡**

  Raspberry Pi 没有内置硬盘，系统启动和所有文件都存储在 **Micro SD 卡** 中。  
  
  .. image:: /_shared/pi_start/img/need_sd.jpg
    :width: 200

  * 最小容量：**16GB**  
  * 推荐容量：**32GB**，稳定性更好  
  * 品牌建议：选择 **SanDisk** 或 **Samsung** 等可靠品牌，以避免读写错误  
  

可选组件
------------------------

虽然不是必需，但以下外设可以显著提升你的学习和调试体验：

* **显示器（HDMI 显示器或电视）**

  对于初学者，强烈建议准备一台带 HDMI 接口的显示器，方便配置 Raspberry Pi OS 并运行图形界面程序。  

  .. image:: /_shared/pi_start/img/need_screen.png
    :width: 400

* **HDMI 线（标准 / Mini / Micro）**
 
  不同型号的 Raspberry Pi 使用不同类型的 HDMI 接口，请根据你的 Pi 型号准备合适的线缆。 
  
  * **Raspberry Pi 4 / 5**：Micro HDMI  
  * **Raspberry Pi 3**：标准 HDMI  
  * **Raspberry Pi Zero 2W**：Mini HDMI  

  .. image:: /_shared/pi_start/img/need_hdmi.png
    :width: 400

* **键盘和鼠标**

  在 Raspberry Pi OS 的初始设置阶段非常有用。后续你可以切换到远程访问（SSH / VNC），但对于初学者，建议先准备一套基础的 USB 或无线键鼠。  

  .. image:: /_shared/pi_start/img/need_keyboard_mouse.png
    :width: 500
 

**准备小贴士**

* 如果你购买的是本套件，大多数配件已经包含，但仍需要另外准备 Raspberry Pi 主板、Micro SD 卡和电源适配器。  
* 不确定该买什么？最稳定、最通用的组合是：**Raspberry Pi 4（2GB）+ 官方电源适配器 + 32GB Micro SD 卡**。  
