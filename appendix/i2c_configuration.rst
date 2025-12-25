.. note::

    ¡Hola! Bienvenido a la comunidad de entusiastas de SunFounder Raspberry Pi, Arduino y ESP32 en Facebook. Sumérgete en el mundo de Raspberry Pi, Arduino y ESP32 con otros entusiastas.

    **¿Por qué unirse?**

    - **Soporte experto**: Resuelve problemas post-venta y desafíos técnicos con la ayuda de nuestra comunidad y equipo.
    - **Aprender y compartir**: Intercambia consejos y tutoriales para mejorar tus habilidades.
    - **Avances exclusivos**: Obtén acceso anticipado a nuevos anuncios de productos y adelantos.
    - **Descuentos especiales**: Disfruta de descuentos exclusivos en nuestros productos más nuevos.
    - **Promociones y sorteos festivos**: Participa en sorteos y promociones festivas.

    👉 ¿Listo para explorar y crear con nosotros? Haz clic en [|link_sf_facebook|] y únete hoy mismo!

.. _i2c_config:

Configuración de I²C
==============================

Sigue los pasos a continuación para habilitar y probar la interfaz I²C en tu Raspberry Pi.  
Estas instrucciones se aplican a Raspberry Pi 5, 4, 3 y Zero 2W.

Habilitar la Interfaz I²C
----------------------------------

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

#. Selecciona **I2C**.

   .. image:: img/ssh_i2c_i2c.png
      :align: center

#. Elige **<Yes>**, luego **<Ok> → <Finish>** para aplicar los cambios.  
   Si se te solicita, reinicia tu Raspberry Pi.

   .. image:: img/ssh_i2c_yes.png
      :align: center


Comprobar los Módulos del Kernel I²C
----------------------------------------------

#. Ejecuta el siguiente comando:

   .. code-block:: bash

      lsmod | grep i2c

#. Si I²C está habilitado, verás módulos como:

   .. code-block:: text

      i2c_dev        6276    0
      i2c_bcm2708    4121    0

#. Si no aparece nada, reinicia el sistema:

   .. code-block:: bash

      sudo reboot


Instalar i2c-tools
----------------------------

#. Instala las utilidades necesarias para escanear y probar dispositivos I²C:

   .. code-block:: bash

      sudo apt install i2c-tools


Detectar Dispositivos I²C Conectados
------------------------------------

#. Escanea el bus I²C:

   .. code-block:: bash

      i2cdetect -y 1

#. Ejemplo de salida:

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

#. Si hay un dispositivo conectado, su dirección (por ejemplo, **0x48**) aparecerá en la tabla.


Instalar la Biblioteca I²C para Python
----------------------------------------------

#. Instala el paquete ``python3-smbus2``:

   .. code-block:: bash

      sudo apt install python3-smbus2

   La biblioteca ``smbus2`` proporciona todas las funciones necesarias para comunicarse con dispositivos I²C en Python.

Tu Raspberry Pi ahora está completamente configurada y lista para comunicarse con dispositivos I²C.
