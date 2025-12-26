.. _setup_pi:

设置你的 Raspberry Pi
======================

在开始编程和控制 Raspberry Pi 之前，你需要先能够访问它。  
本指南介绍两种常见的方法：

* 使用显示器、键盘和鼠标  
* 使用无屏幕（Headless）的远程访问方式  

.. note::

   安装在机器人上的 Raspberry Pi Zero 2W 不方便连接显示器。  
   我们推荐使用 **无屏幕（Headless）配置** 的方式。

-------------------------
如果你有显示器
-------------------------

**所需组件**

* Raspberry Pi
* 官方电源适配器
* MicroSD 卡
* HDMI 线  
  （对于 Raspberry Pi 4/5，请使用 **HDMI0**，即最靠近电源接口的那个端口）
* 显示器
* 键盘和鼠标

**步骤**

#. 将 microSD 卡插入 Raspberry Pi。
#. 连接键盘、鼠标和显示器。
#. 给 Raspberry Pi 上电。
#. 启动完成后，将显示 Raspberry Pi OS 的桌面。 

   .. image:: /_shared/pi_start/img/plug_screen_trixie.png
      :width: 80%
      :align: center

#. 打开 **终端（Terminal）** 来输入命令。

   .. image:: /_shared/pi_start/img/open_terminal.png
      :width: 80%
      :align: center


----------------------------------
如果你没有显示器（Headless）
----------------------------------

在没有显示器的情况下，你可以通过远程方式配置并登录 Raspberry Pi。  
这是大多数用户最方便的方式。

**所需组件**

* Raspberry Pi
* 官方电源适配器
* MicroSD 卡
* 一台位于同一网络中的电脑

**提示**

* 使用 Raspberry Pi Imager 安装系统时，请确保已完成 :ref:`imager_custom` 中描述的所有设置。
* 确保 Raspberry Pi 和你的电脑在同一个本地网络中。
* 为了获得最佳稳定性，如条件允许，建议使用有线以太网。


**通过 SSH 连接**

#. 在你的电脑上打开终端（Windows：**PowerShell**；macOS/Linux：**Terminal**），并连接到 Raspberry Pi：

   .. code-block:: bash

      ssh <username>@<hostname>.local
      # 示例：
      ssh daisy@pi.local

2. 或者，从路由器的 DHCP 列表中查找 Raspberry Pi 的 IP 地址，然后使用以下方式连接：

   .. code-block:: bash

      ssh <username>@<IP address>
      # 示例：
      ssh daisy@192.168.1.42

3. 首次登录时，输入 ``yes`` 以确认 SSH 证书。

4. 输入你在 Raspberry Pi Imager 中设置的密码。  
   （输入时不会显示字符，这是正常现象。）

5. 登录成功后，你将获得完整的命令行访问权限。

   .. image:: /_shared/pi_start/img/ssh_login.png
      :align: center

----------------------

**故障排查**

* **ssh: Could not resolve hostname ...**

  * 请确认主机名是否正确。
  * 尝试使用 Raspberry Pi 的 IP 地址进行连接。

* **The term 'ssh' is not recognized...（Windows）**

  * 未安装 OpenSSH。请手动安装，或使用第三方 SSH 客户端。  
  * 参见 :ref:`openssh_powershell` 或 :ref:`login_windows`。

* **Permission denied (publickey,password)**

  * 请确认你使用的是在 Raspberry Pi Imager 中创建的用户名和密码。

* **Connection refused**

  * 上电后等待 1–2 分钟再尝试连接。
  * 确认已在 Raspberry Pi Imager 中启用了 SSH。

--------------------------------

图形化远程访问方式
---------------------

.. |shared_link_rpi_connect| raw:: html

    <a href="https://www.raspberrypi.com/documentation/services/connect.html" target="_blank">Raspberry Pi Connect</a> 

如果你更偏好图形界面：

* :ref:`remote_desktop`：启用 **VNC（虚拟网络计算）**，以获得完整的 Raspberry Pi 桌面体验。

* |shared_link_rpi_connect|：使用 Raspberry Pi Connect，通过浏览器从任何地方安全地远程访问你的 Raspberry Pi。 

现在，你无需显示器即可控制 Raspberry Pi：  
可以通过 SSH 进行命令行操作，或通过 VNC / Raspberry Pi Connect 使用图形化桌面。
