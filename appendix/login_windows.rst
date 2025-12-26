
.. _login_windows:

PuTTY
=========================

PuTTY 是一款简单且可靠的 SSH 客户端，适用于 Windows 用户远程访问 Raspberry Pi。  


.. |shared_link_putty| raw:: html

    <a href="https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html>" target="_blank">PuTTY</a> 


#. 从 |shared_link_putty| 下载 PuTTY 并在你的电脑上安装。

   .. image:: /_shared/appendix/img/putty_download.png
      :width: 70%


#. 打开 PuTTY 并准备连接：

   * 在 **Host Name** 中输入你的 Raspberry Pi 的 **主机名或 IP 地址**。
   * 将 **Port** 设置为 ``22``。
   * 点击 **Open** 进行连接。


   .. image:: /_shared/appendix/img/putty_open.png
      :width: 70%
   
#. 如果首次使用时出现安全警告，点击 **Accept** 继续。

   .. image:: /_shared/appendix/img/putty_accept.png
      :width: 70%

#. 登录 Raspberry Pi：

   * 当看到 **login as:** 提示时，输入你在 **Raspberry Pi Imager** 中设置的用户名。
   * 输入密码（输入时不会显示字符，这是正常现象）。
   * 登录成功后，终端即可使用，你可以远程输入命令并操作 Raspberry Pi。

   .. image:: /_shared/appendix/img/putty_login.png
      :width: 70%

.. note::

    如果 PuTTY 显示 **inactive**，说明连接已断开，需要重新连接。
