.. note::

    ¡Hola! Bienvenido a la comunidad de entusiastas de SunFounder Raspberry Pi, Arduino y ESP32 en Facebook. Sumérgete en el mundo de Raspberry Pi, Arduino y ESP32 con otros entusiastas.

    **¿Por qué unirse?**

    - **Soporte experto**: Resuelve problemas post-venta y desafíos técnicos con la ayuda de nuestra comunidad y equipo.
    - **Aprender y compartir**: Intercambia consejos y tutoriales para mejorar tus habilidades.
    - **Avances exclusivos**: Obtén acceso anticipado a nuevos anuncios de productos y adelantos.
    - **Descuentos especiales**: Disfruta de descuentos exclusivos en nuestros productos más nuevos.
    - **Promociones y sorteos festivos**: Participa en sorteos y promociones festivas.

    👉 ¿Listo para explorar y crear con nosotros? Haz clic en [|link_sf_facebook|] y únete hoy mismo!

.. _remote_desktop:

Escritorio Remoto
=======================

.. |shared_link_realvnc| raw:: html

    <a href="https://www.realvnc.com/en/connect/download/viewer/" target="_blank">RealVNC® Viewer</a>   

Puedes acceder y controlar el escritorio de la Raspberry Pi de forma remota desde otro ordenador.  
El método recomendado es **VNC**, que cuenta con soporte oficial en Raspberry Pi OS y ofrece una experiencia de escritorio fiable y consistente.

La siguiente sección explica cómo habilitar VNC en tu Raspberry Pi y conectarte a ella usando |shared_link_realvnc|.

-----------------

Habilitar el Servicio VNC
---------------------------------

RealVNC Server viene preinstalado en Raspberry Pi OS, pero está **deshabilitado por defecto**.  
Debes habilitarlo mediante la herramienta de configuración.

#. Abre una terminal en tu ordenador (Windows: **PowerShell**; macOS/Linux: **Terminal**) y conéctate a tu Raspberry Pi:

   .. code-block:: bash

      ssh <usuario>@<hostname>.local

   o

   .. code-block:: bash

      ssh <usuario>@<dirección_ip>

#. Ejecuta la herramienta de configuración:

   .. code-block:: bash

      sudo raspi-config

   .. image:: /_shared/appendix/img/ssh_raspi_config.png


#. Selecciona **Interfacing Options** y presiona **Enter**.

   .. image:: /_shared/appendix/img/ssh_interface.png


#. Selecciona **VNC**.

   .. image:: /_shared/appendix/img/ssh_vnc_vnc.png


#. Elige **Yes**, luego **OK**, y finalmente **Finish** para salir.

   .. image:: /_shared/appendix/img/ssh_vnc_enable.png



Iniciar Sesión con RealVNC® Viewer
------------------------------------

#. Descarga e instala |shared_link_realvnc| para tu sistema operativo.

   .. image:: /_shared/appendix/img/ssh_vnc_download.png


#. Abre **RealVNC Viewer**, introduce la dirección IP de tu Raspberry Pi o ``<hostname>.local`` y presiona **Enter**.

   .. image:: /_shared/appendix/img/ssh_vnc_login.png


#. Introduce el **nombre de usuario** y la **contraseña** de tu Raspberry Pi, luego selecciona **OK**.

   .. note::

      Al conectarte por primera vez, puede aparecer un mensaje como “VNC Server not recognized”. Selecciona **Continue** para continuar.

   .. image:: /_shared/appendix/img/ssh_vnc_username.png


#. Ahora deberías ver el escritorio de la Raspberry Pi:

   .. image:: /_shared/appendix/img/ssh_vnc_desktop.png


Esto completa el proceso de configuración de VNC.

-----------------


Notas Adicionales
--------------------

* **Se requiere la versión de escritorio**

  * VNC requiere que la Raspberry Pi ejecute la versión completa de escritorio de Raspberry Pi OS.  
  * Si estás usando **Raspberry Pi OS Lite**, instala VNC Server manualmente: ``sudo apt install realvnc-vnc-server``


* **Consejos de rendimiento de red** 

  * Si experimentas retrasos o una actualización lenta de la pantalla, revisa la calidad de tu red.  
  * La conexión por Ethernet cableada suele ofrecer el mejor rendimiento.


* **Solucionar problemas de resolución de pantalla**

  * Si la ventana de VNC aparece demasiado pequeña o la resolución es incorrecta, configura una resolución fija en: ``sudo raspi-config`` → **Display Options** → **VNC Resolution**


* **Asegúrate de que VNC esté habilitado**

  Si VNC no logra conectarse, verifica que esté habilitado en: ``sudo raspi-config`` → ``Interfacing Options`` → ``VNC``

* **Detener el servicio VNC**

  Para detener manualmente el servidor VNC: ``sudo systemctl stop vncserver-x11-serviced``


* **Recordatorio de seguridad**

  * VNC está diseñado para redes locales de confianza.  
  * **No** expongas VNC directamente a Internet.  
  * Para acceso remoto seguro desde fuera de tu red, utiliza **Raspberry Pi Connect** o una VPN.
