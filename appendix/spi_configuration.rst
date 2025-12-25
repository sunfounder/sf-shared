.. note::

    ¡Hola! Bienvenido a la comunidad de entusiastas de SunFounder Raspberry Pi, Arduino y ESP32 en Facebook. Sumérgete en el mundo de Raspberry Pi, Arduino y ESP32 con otros entusiastas.

    **¿Por qué unirse?**

    - **Soporte experto**: Resuelve problemas post-venta y desafíos técnicos con la ayuda de nuestra comunidad y equipo.
    - **Aprender y compartir**: Intercambia consejos y tutoriales para mejorar tus habilidades.
    - **Avances exclusivos**: Obtén acceso anticipado a nuevos anuncios de productos y adelantos.
    - **Descuentos especiales**: Disfruta de descuentos exclusivos en nuestros productos más nuevos.
    - **Promociones y sorteos festivos**: Participa en sorteos y promociones festivas.

    👉 ¿Listo para explorar y crear con nosotros? Haz clic en [|link_sf_facebook|] y únete hoy mismo!


.. _spi_configuration:

Configuración de SPI
===============================

Sigue los pasos a continuación para habilitar y verificar la interfaz SPI en tu Raspberry Pi.  
Estas instrucciones se aplican a Raspberry Pi 5, 4, 3 y Zero 2W.

Habilitar la Interfaz SPI
---------------------------------

#. Abre una terminal en tu ordenador (Windows: **PowerShell**; macOS/Linux: **Terminal**) y conéctate a tu Raspberry Pi:

   .. code-block:: bash

      ssh <usuario>@<hostname>.local

   o:

   .. code-block:: bash

      ssh <usuario>@<dirección_ip>

#. Abre la herramienta de configuración de Raspberry Pi:

   .. code-block:: bash

      sudo raspi-config

#. Selecciona **Interfacing Options** y presiona **Enter**.

   .. image:: /_shared/appendix/img/ssh_interface.png
      :align: center

#. Selecciona **SPI**.

   .. image:: img/ssh_spi_spi.png
      :align: center

#. Elige **<Yes>**, luego **<Ok> → <Finish>** para aplicar los cambios. Si se te solicita, reinicia tu Raspberry Pi.

   .. image:: img/ssh_spi_enable.png
      :align: center


Verificar la Interfaz SPI
--------------------------------

#. Comprueba si existen los nodos de dispositivo SPI:

   .. code-block:: bash

      ls /dev/sp*

#. Si la interfaz SPI está habilitada, la salida incluirá:

   .. code-block:: text

      /dev/spidev0.0
      /dev/spidev0.1

   * Si aparecen estos dispositivos, SPI está activo y listo para usarse.  
   * Si no aparecen, reinicia tu Raspberry Pi y vuelve a comprobarlo.


Instalar spidev (Biblioteca SPI para Python)
-----------------------------------------------------

#. Instala el paquete ``spidev`` para usar SPI en Python:

   .. code-block:: bash

      sudo apt install python3-spidev

   La biblioteca ``spidev`` proporciona acceso a dispositivos SPI a través de la interfaz ``/dev/spidevX.Y``.

----------------------

Tu Raspberry Pi ahora está configurada para comunicarse con dispositivos SPI tanto mediante herramientas de línea de comandos como con Python.
