
.. _spi_configuration:

SPI 配置
===================

按照以下步骤在你的 Raspberry Pi 上启用并验证 SPI 接口。  
这些说明适用于 Raspberry Pi 5、4、3 以及 Zero 2W。

启用 SPI 接口
--------------

#. 在你的电脑上打开终端（Windows：**PowerShell**；macOS/Linux：**Terminal**），并连接到 Raspberry Pi：

   .. code-block:: bash

      ssh <username>@<hostname>.local

   或者：

   .. code-block:: bash

      ssh <username>@<ip_address>

#. 打开 Raspberry Pi 配置工具：

   .. code-block:: bash

      sudo raspi-config

#. 选择 **Interfacing Options**，然后按 **Enter**。

   .. image:: /_shared/appendix/img/ssh_interface.png
      :align: center

#. 选择 **SPI**。

   .. image:: img/ssh_spi_spi.png
      :align: center

#. 选择 **<Yes>**，然后依次选择 **<Ok> → <Finish>** 以应用更改。如系统提示，请重启 Raspberry Pi。

   .. image:: img/ssh_spi_enable.png
      :align: center


验证 SPI 接口
--------------

#. 检查 SPI 设备节点是否存在：

   .. code-block:: bash

      ls /dev/sp*

#. 如果 SPI 接口已启用，输出中将包含：

   .. code-block:: text

      /dev/spidev0.0
      /dev/spidev0.1

   * 如果看到这些设备节点，说明 SPI 已启用并可以使用。  
   * 如果没有显示，请重启 Raspberry Pi 后再次检查。


安装 spidev（Python SPI 库）
----------------------------

#. 安装 ``spidev`` 软件包，以便在 Python 中使用 SPI：

   .. code-block:: bash

      sudo apt install python3-spidev

   ``spidev`` 库通过 ``/dev/spidevX.Y`` 接口提供对 SPI 设备的访问。

----------------------

现在，你的 Raspberry Pi 已完成配置，可以通过命令行工具和 Python 与 SPI 设备进行通信。

