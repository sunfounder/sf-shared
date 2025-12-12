.. note::

    Hello, welcome to the SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasts Community on Facebook! Dive deeper into Raspberry Pi, Arduino, and ESP32 with fellow enthusiasts.

    **Why Join?**

    - **Expert Support**: Solve post-sale issues and technical challenges with help from our community and team.
    - **Learn & Share**: Exchange tips and tutorials to enhance your skills.
    - **Exclusive Previews**: Get early access to new product announcements and sneak peeks.
    - **Special Discounts**: Enjoy exclusive discounts on our newest products.
    - **Festive Promotions and Giveaways**: Take part in giveaways and holiday promotions.

    👉 Ready to explore and create with us? Click [|link_sf_facebook|] and join today!

.. _login_windows:

PuTTY
=========================

PuTTY is a simple and reliable SSH client for Windows users to remotely access the Raspberry Pi.  


.. |shared_link_putty| raw:: html

    <a href="https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html>" target="_blank">PuTTY</a> 


#. Download PuTTY from |shared_link_putty| and install it on your computer.

   .. image:: /_shared/appendix/img/putty_download.png
      :width: 70%


#. Open PuTTY and prepare the connection:

   * Enter your Raspberry Pi’s **hostname or IP address** in **Host Name**.
   * Set the **Port** to ``22``.
   * Click **Open** to connect.


   .. image:: /_shared/appendix/img/putty_open.png
      :width: 70%
   
#. If a security warning appears on first use, click **Accept** to continue.

   .. image:: /_shared/appendix/img/putty_accept.png
      :width: 70%

#. Log in to the Raspberry Pi:

   * When you see **login as:**, enter the username you set in **Raspberry Pi Imager**.
   * Enter your password (it will not appear while typing—this is normal).
   * After logging in, the terminal is ready for you to enter commands and operate your Raspberry Pi remotely.

   .. image:: /_shared/appendix/img/putty_login.png
      :width: 70%

.. note::

    If PuTTY shows **inactive**, the connection was lost and needs to be reconnected.
