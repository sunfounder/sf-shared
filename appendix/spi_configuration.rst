.. note::

    Hello, welcome to the SunFounder Raspberry Pi, Arduino, and ESP32 Enthusiasts Community on Facebook!  
    Join fellow makers to explore, learn, and create together.

    **Why Join?**

    - **Expert Support** — Get help with post-sale issues and technical challenges.
    - **Learn & Share** — Exchange tutorials, tips, and hands-on experiences.
    - **Exclusive Previews** — Get early access to new product announcements.
    - **Special Discounts** — Enjoy members-only offers on new products.
    - **Giveaways & Events** — Join festive promotions and prize draws.

    👉 Click |link_sf_facebook| to join the community!


.. _spi_configuration:

SPI Configuration
=================

Follow the steps below to enable and verify the SPI interface on your Raspberry Pi.  
These instructions apply to Raspberry Pi 5, 4, 3, and Zero 2W.

Enable the SPI Interface
------------------------

#. Open a terminal on your computer (Windows: **PowerShell**; macOS/Linux: **Terminal**) and connect to your Raspberry Pi:

   .. code-block:: bash

      ssh <username>@<hostname>.local

   or:

   .. code-block:: bash

      ssh <username>@<ip_address>

#. Open the Raspberry Pi configuration tool:

   .. code-block:: bash

      sudo raspi-config

#. Select **Interfacing Options** and press **Enter**.

   .. image:: /_shared/appendix/img/ssh_interface.png
      :align: center

#. Select **SPI**.

   .. image:: img/ssh_spi_spi.png
      :align: center

#. Choose **<Yes>**, then **<Ok> → <Finish>** to apply the changes. If prompted, reboot your Raspberry Pi.

   .. image:: img/ssh_spi_enable.png
      :align: center


Verify SPI Interface
---------------------

#. Check whether the SPI device nodes exist:

   .. code-block:: bash

      ls /dev/sp*

#. If the SPI interface is enabled, the output will include:

   .. code-block:: text

      /dev/spidev0.0
      /dev/spidev0.1

   * If these devices appear, SPI is active and ready to use.  
   * If not, reboot your Raspberry Pi and check again.


Install spidev (Python SPI Library)
-----------------------------------

#. Install the ``spidev`` package to use SPI in Python:

   .. code-block:: bash

      sudo apt install python3-spidev

   The ``spidev`` library provides access to SPI devices through the ``/dev/spidevX.Y`` interface.

----------------------

Your Raspberry Pi is now configured to communicate with SPI devices using both command-line tools and Python.


