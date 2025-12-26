

.. _install_all_modules_fusion_hat:

配置电源并安装软件（重要）
================================================================

在本章节中，你将安装相关软件、配置音频、设置安全的电源管理方式，并学习如何正确关机。

.. start_install_fusion_hat

.. _install_fusion_hat:

安装 ``fusion-hat`` 模块
----------------------------------

在本套件中，所有 GPIO 功能都通过 Fusion HAT+ 进行管理。因此，你需要使用配套的 ``fusion-hat`` 库来访问和控制这些功能。

请在终端中运行以下命令以安装 ``fusion-hat`` 模块。

   .. raw:: html

      <run></run>

   .. code-block::

      curl -sSL https://raw.githubusercontent.com/sunfounder/sunfounder-installer-scripts/main/install-fusion-hat.sh | sudo bash

.. |shared_link_fusion_hat| raw:: html

    <a href="https://docs.sunfounder.com/projects/fusion-hat/en/latest/" target="_blank">Fusion HAT+</a>

.. note::  
   有关 fusion-hat 的详细说明，请参考 |shared_link_fusion_hat|。

安装完成后，请重启 Raspberry Pi。随后执行音频设置脚本：

   .. raw:: html

      <run></run>

   .. code-block::

      sudo /opt/setup_fusion_hat_audio.sh

至此，Fusion HAT+ 的软件安装过程完成。


配置并使用安全关机
---------------------

Fusion HAT+ 依赖 Raspberry Pi 的关机信号来完成电源的全面管理。  
为了确保安全、可靠的断电过程，你需要根据 Raspberry Pi 的型号 **配置关机行为**，并正确使用 **电源按钮**。

**适用于 Raspberry Pi 5 和 4B**

这些型号在关机后支持完全断电。Fusion HAT+ 通过监测 3.3V 电源线来判断 Raspberry Pi 的电源状态。

1. 将跳线帽插在 **RPI_STATE → Pi3V3** 上。

   .. image:: /_shared/pi_start/img/state_3v3.jpg
      :width: 400

2. 手动编辑 EEPROM 配置：

   .. code-block::

      sudo raspi-config

3. 进入 **Advanced Options → A12 Shutdown Behaviour**。

   .. image:: /_shared/pi_start/img/shutdown_behaviour.png

4. 选择 **B1 Full Power Off**。

   .. image:: /_shared/pi_start/img/run_power_off.png

5. 保存更改。系统会提示你重启以使新设置生效。

**适用于 Raspberry Pi Zero 2W、3B、3B+**

这些型号 **不支持** 通过 3.3V 实现完全断电，而是需要将 GPIO26 配置为关机状态指示引脚。

1. 将跳线帽插在 **RPI_STATE → IO26** 上。

   .. image:: /_shared/pi_start/img/state_io26.jpg
      :width: 400

2. 编辑 ``/boot/firmware/config.txt`` 文件：

   .. code-block::

      sudo nano /boot/firmware/config.txt

3. 在文件末尾添加以下内容，使 GPIO26 在关机时为低电平、开机时为高电平：

   .. code-block::

      dtoverlay=gpio-poweroff,gpio_pin=26,active_low=1

4. 重启系统以应用设置：

   .. code-block::

      sudo reboot


**使用电源按钮进行安全关机**

完成关机配置后，你就可以通过 Fusion HAT+ 的电源按钮安全地关闭 PiCar-X。

* **软关机（推荐）**

  * 长按电源按钮 **2 秒**。  
  * 两个电源指示灯会快速闪烁。  
  * 松开按钮 → Fusion HAT+ 触发 Raspberry Pi 正常关机。  
  * 关机完成后，Fusion HAT+ 会自动切断电源。  
  * 这种方式可以有效保护 SD 卡和系统文件。

* **硬关机（仅限紧急情况）**

  * 当系统无响应时，长按电源按钮 **5 秒以上**。  
  * Fusion HAT+ 将强制断电。  
  * 警告：此操作可能导致 SD 卡或系统文件损坏，仅在必要时使用。

.. end_install_fusion_hat
