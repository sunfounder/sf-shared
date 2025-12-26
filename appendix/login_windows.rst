
.. _login_windows:

PuTTY
=========================

PuTTY is a simple and reliable SSH client for Windows users to remotely access the Raspberry Pi.  

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
