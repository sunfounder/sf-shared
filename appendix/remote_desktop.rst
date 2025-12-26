
.. _remote_desktop:

远程桌面
========

.. |shared_link_realvnc| raw:: html

    <a href="https://www.realvnc.com/en/connect/download/viewer/" target="_blank">RealVNC® Viewer</a>   

你可以从另一台电脑远程访问并控制 Raspberry Pi 的桌面。  
推荐的方法是 **VNC**，它在 Raspberry Pi OS 中得到官方支持，能够提供稳定、一致的桌面体验。

以下内容将介绍如何在 Raspberry Pi 上启用 VNC，并使用 |shared_link_realvnc| 进行连接。

-----------------

启用 VNC 服务
--------------

RealVNC Server 已预装在 Raspberry Pi OS 中，但 **默认是关闭的**。  
你需要通过配置工具将其启用。

#. 在你的电脑上打开终端（Windows：**PowerShell**；macOS/Linux：**Terminal**），并连接到 Raspberry Pi：

   .. code-block:: bash

      ssh <username>@<hostname>.local

   或

   .. code-block:: bash

      ssh <username>@<ip_address>

#. 运行配置工具：

   .. code-block:: bash

      sudo raspi-config

   .. image:: /_shared/appendix/img/ssh_raspi_config.png


#. 选择 **Interfacing Options**，然后按 **Enter**。

   .. image:: /_shared/appendix/img/ssh_interface.png


#. 选择 **VNC**。

   .. image:: /_shared/appendix/img/ssh_vnc_vnc.png


#. 选择 **Yes**，然后依次点击 **OK**，最后选择 **Finish** 退出。

   .. image:: /_shared/appendix/img/ssh_vnc_enable.png



使用 RealVNC® Viewer 登录
--------------------------

#. 下载并安装适用于你操作系统的 |shared_link_realvnc|。

   .. image:: /_shared/appendix/img/ssh_vnc_download.png


#. 打开 **RealVNC Viewer**，输入 Raspberry Pi 的 IP 地址或 ``<hostname>.local``，然后按 **Enter**。

   .. image:: /_shared/appendix/img/ssh_vnc_login.png


#. 输入 Raspberry Pi 的 **用户名** 和 **密码**，然后选择 **OK**。

   .. note::

      首次连接时，可能会看到类似 “VNC Server not recognized” 的提示，选择 **Continue** 即可继续。

   .. image:: /_shared/appendix/img/ssh_vnc_username.png


#. 此时你应该可以看到 Raspberry Pi 的桌面：

   .. image:: /_shared/appendix/img/ssh_vnc_desktop.png


至此，VNC 的设置过程已完成。

-----------------


附加说明
--------

* **需要桌面版系统**

  * VNC 需要 Raspberry Pi 运行完整的桌面版 Raspberry Pi OS。  
  * 如果你使用的是 **Raspberry Pi OS Lite**，请手动安装 VNC Server：``sudo apt install realvnc-vnc-server``


* **网络性能建议**

  * 如果出现卡顿或刷新率较低的情况，请检查网络质量。  
  * 有线以太网通常能提供最佳性能。


* **解决显示分辨率问题**

  * 如果 VNC 窗口显示过小或分辨率不正确，可通过以下路径设置固定分辨率：  
    ``sudo raspi-config`` → **Display Options** → **VNC Resolution**


* **确认 VNC 已启用**

  如果 VNC 无法连接，请确认在以下位置已启用：  
  ``sudo raspi-config`` → ``Interfacing Options`` → ``VNC``


* **停止 VNC 服务**

  如需手动停止 VNC Server，可运行：  
  ``sudo systemctl stop vncserver-x11-serviced``


* **安全提醒**

  * VNC 适用于受信任的本地网络环境。  
  * 请 **不要** 将 VNC 直接暴露在公网中。  
  * 若需要从外部网络安全访问，建议使用 **Raspberry Pi Connect** 或 VPN。
