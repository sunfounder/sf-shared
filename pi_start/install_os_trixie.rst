
.. _install_os:

安装操作系统
===================

.. start_imager

在使用 Raspberry Pi 之前，你需要将 **Raspberry Pi OS** 安装到一张 microSD 卡中。  
本指南将以简单、适合初学者的方式，介绍如何使用 **Raspberry Pi Imager** 完成安装。

**所需组件**

* 一台电脑（Windows、macOS 或 Linux）
* 一张 microSD 卡（16GB 或更大；推荐品牌：SanDisk、Samsung）
* 一个 microSD 读卡器

-------------------

**1. 安装 Raspberry Pi Imager**
-------------------------------------------


.. |shared_link_rpi_imager| raw:: html

    <a href="https://www.raspberrypi.com/software/" target="_blank">Raspberry Pi Imager</a>   

#. 访问 Raspberry Pi Imager 官方下载页面：|shared_link_rpi_imager|，下载适用于你操作系统的安装程序。

   .. image:: /_shared/pi_start/img/imager_download.png
      :width: 70%

#. 按照安装提示完成安装（语言、安装路径、确认等）。安装完成后，从桌面或应用程序菜单中启动 **Raspberry Pi Imager**。

   .. image:: /_shared/pi_start/img/imager_install.png
      :width: 90%

-------------------

**2. 将操作系统写入 microSD 卡**
------------------------------------------------

1. 使用读卡器将 microSD 卡插入电脑。在继续之前，请先备份卡中任何重要数据。

   .. image:: /_shared/pi_start/img/insert_sd.png
      :width: 90%

2. 打开 Raspberry Pi Imager 后，你会看到 **Device** 页面。从列表中选择你的 Raspberry Pi 型号（例如 Raspberry Pi 5、4、3 或 Zero 2W）。

   .. image:: /_shared/pi_start/img/imager_device.png
      :width: 90%

   .. end_imager

3. 进入 **OS** 选项，选择推荐的 **Raspberry Pi OS (64-bit)**。

   .. image:: /_shared/pi_start/img/imager_os.png
      :width: 90%

   .. start_choose_os

4. 在 **Storage** 选项中，选择你的 microSD 卡。为安全起见，建议拔掉其他 USB 存储设备，确保列表中只显示 SD 卡。

   .. image:: /_shared/pi_start/img/imager_storage.png
      :width: 90%

5. 点击 **Next** 进入自定义设置步骤。

   .. note::

      * 如果你将直接为 Raspberry Pi 连接显示器、键盘和鼠标，可以点击 **SKIP CUSTOMISATION**。  
      * 如果你计划以 **无头模式** （通过 Wi-Fi 远程访问）设置 Raspberry Pi，则必须完成自定义设置。

   .. image:: /_shared/pi_start/img/imager_custom_skip.png
      :width: 90%

-------------------

.. _imager_custom:

**3. 操作系统自定义设置**
------------------------------------------

#. **设置主机名（Hostname）**

   * 为你的 Raspberry Pi 设置一个唯一的主机名。  
   * 之后你可以通过 ``hostname.local`` 来连接它。

   .. image:: /_shared/pi_start/img/imager_custom_hostname.png
      :width: 90%

#. **设置本地化（Localisation）**

   * 选择你所在的首都城市。
   * Imager 会根据你的选择自动补全时区和键盘布局，你也可以根据需要进行调整。然后选择 Next。
   
   .. image:: /_shared/pi_start/img/imager_custom_local.png
      :width: 90%

#. **设置用户名和密码**

   为你的 Raspberry Pi 创建一个用户账户。
   
   .. image:: /_shared/pi_start/img/imager_custom_user.png
      :width: 90%

#. **配置 Wi-Fi**

   * 输入你的 Wi-Fi **SSID**（网络名称）和 **密码**。  
   * Raspberry Pi 在首次启动时会自动连接该网络。
   
   .. image:: /_shared/pi_start/img/imager_custom_wifi.png
      :width: 90%

#. **启用 SSH（可选但推荐）**

   * 启用 SSH 后，你可以从电脑远程登录 Raspberry Pi。  
   * 你可以使用用户名/密码登录，或配置 SSH 密钥。
   
   .. image:: /_shared/pi_start/img/imager_custom_ssh.png
      :width: 90%

#. **启用 Raspberry Pi Connect（可选）**


   Raspberry Pi Connect 允许你通过网页浏览器访问 Raspberry Pi 的桌面。
   
   * 打开 **Raspberry Pi Connect**，然后点击 **OPEN RASPBERRY PI CONNECT**。
   
     .. image:: /_shared/pi_start/img/imager_custom_connect.png
        :width: 90%

   * Raspberry Pi Connect 网站会在默认浏览器中打开。登录你的 Raspberry Pi ID 账户；如果还没有账户，请先注册。

     .. image:: /_shared/pi_start/img/imager_custom_open.png
        :width: 90%

   * 在 **New auth key** 页面中，创建一次性授权密钥。
      
      * 如果你的 Raspberry Pi ID 账户不属于任何组织，选择 **Create auth key and launch Raspberry Pi Imager**。
      * 如果你属于一个或多个组织，请选择其中一个，然后创建密钥并启动 Imager。
      * 请确保在密钥过期之前，给 Raspberry Pi 上电并连接到互联网。
   
     .. image:: /_shared/pi_start/img/imager_custom_authkey.png
        :width: 90%
   
   * 浏览器可能会询问是否打开 Raspberry Pi Imager，请允许。

     * Imager 将在 Raspberry Pi Connect 标签页中打开，并显示认证令牌。
     * 如果令牌没有自动传递，请在 Raspberry Pi Connect 页面中打开 **Having trouble?** 部分，复制令牌并手动粘贴到 Imager 中。

     .. image:: /_shared/pi_start/img/imager_custom_connect_token.png
        :width: 90%

-------------------

**4. 写入操作系统镜像**


#. 检查所有设置无误后，点击 **WRITE**。

   .. image:: /_shared/pi_start/img/imager_writing.png
      :width: 90%

#. 如果存储卡中已有数据，Raspberry Pi Imager 会提示设备上的所有数据将被擦除。请再次确认你选择的是正确的驱动器，然后点击 **I UNDERSTAND, ERASE AND WRITE** 继续。

   .. image:: /_shared/pi_start/img/imager_erase.png
      :width: 90%

#. 等待写入和校验完成。完成后，Raspberry Pi Imager 会显示 **Write complete!** 以及你的设置摘要。存储设备会自动弹出，你可以安全取出。

   .. image:: /_shared/pi_start/img/imager_finish.png
        :width: 90%

#. 取出 microSD 卡，并将其插入 Raspberry Pi 底部的卡槽中。现在你的 Raspberry Pi 已准备好使用新的操作系统启动了！

   .. image:: /_shared/pi_start/img/os_sd_to_pi.jpg
        :width: 70%

   .. end_choose_os

