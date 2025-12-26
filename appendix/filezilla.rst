
.. _filezilla:

FileZilla 软件
===============

.. image:: /_shared/appendix/img/filezilla_icon.png
   :width: 20%

文件传输协议（FTP）通常用于在网络中不同计算机之间传输文件。 **FileZilla** 是一款开源客户端，支持 FTP、FTPS 以及 **SFTP** （推荐用于 Raspberry Pi）。  
通过 FileZilla，你可以轻松地将文件（如图片、音频和脚本）从电脑上传到 Raspberry Pi，或将文件从 Raspberry Pi 下载到电脑。

下载 FileZilla
---------------

.. |shared_link_filezilla| raw:: html

    <a href="https://filezilla-project.org/" target="_blank">FileZilla</a> 

#. 访问 |shared_link_filezilla| 官方网站，下载适用于你操作系统的 **FileZilla Client**。

#. 安装并启动该程序。

   .. image:: /_shared/appendix/img/filezilla_install.png

#. 打开 FileZilla，输入以下信息：

   * **Host：** ``<hostname>.local`` 或 Raspberry Pi 的 IP 地址  
   * **Username：** 你的 Pi 用户名  
   * **Password：** 在 Raspberry Pi Imager 中设置的密码  
   * **Port：** ``22`` （用于 SFTP）
   * 点击 **Quickconnect** （或按 **Enter**）建立连接。

   .. image:: /_shared/appendix/img/filezilla_connect.png
      :align: center

#. 连接成功后，左侧面板显示你的 **本地文件**，右侧面板显示 **Raspberry Pi 上的文件**。

    .. image:: /_shared/appendix/img/filezilla_in.png
       :align: center

#. 你可以：

   * **上传文件：** 从左侧面板拖拽到右侧面板  
   * **下载文件：** 从右侧面板拖拽到左侧面板  

   FileZilla 会立即开始传输，传输状态会显示在底部的状态面板中。
