
.. _i2c_config:

I²C 配置
=============

按照以下步骤在你的 Raspberry Pi 上启用并测试 I²C 接口。  
这些说明适用于 Raspberry Pi 5、4、3 以及 Zero 2W。

启用 I²C 接口
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

#. 选择 **I2C**。

   .. image:: img/ssh_i2c_i2c.png
      :align: center

#. 选择 **<Yes>**，然后依次选择 **<Ok> → <Finish>** 以应用更改。  
   如果系统提示，请重启 Raspberry Pi。

   .. image:: img/ssh_i2c_yes.png
      :align: center


检查 I²C 内核模块
------------------

#. 运行以下命令：

   .. code-block:: bash

      lsmod | grep i2c

#. 如果 I²C 已启用，你会看到类似下面的模块：

   .. code-block:: text

      i2c_dev        6276    0
      i2c_bcm2708    4121    0

#. 如果没有任何输出，请重启系统：

   .. code-block:: bash

      sudo reboot


安装 i2c-tools
---------------

#. 安装用于扫描和测试 I²C 设备的工具：

   .. code-block:: bash

      sudo apt install i2c-tools


检测已连接的 I²C 设备
----------------------

#. 扫描 I²C 总线：

   .. code-block:: bash

      i2cdetect -y 1

#. 示例输出：

   .. code-block:: text

      pi@raspberrypi ~ $ i2cdetect -y 1
          0  1  2  3   4  5  6  7  8  9   a  b  c  d  e  f
      00:           -- -- -- -- -- -- -- -- -- -- -- -- --
      10: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --
      20: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --
      30: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --
      40: -- -- -- -- -- -- -- -- 48 -- -- -- -- -- -- --
      50: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --
      60: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --
      70: -- -- -- -- -- -- -- --

#. 如果有设备连接，其地址（例如 **0x48**）将显示在表格中。


安装 Python I²C 库
------------------

#. 安装 ``python3-smbus2`` 软件包：

   .. code-block:: bash

      sudo apt install python3-smbus2

   ``smbus2`` 库提供了在 Python 中与 I²C 设备通信所需的全部函数。

现在，你的 Raspberry Pi 已完成配置，可以与 I²C 设备进行通信了。
