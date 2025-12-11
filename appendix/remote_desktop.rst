.. note::

    ¡Hola, bienvenido a la comunidad de entusiastas de SunFounder Raspberry Pi & Arduino & ESP32 en Facebook! Sumérgete más en Raspberry Pi, Arduino y ESP32 con otros entusiastas.

    **¿Por qué unirse?**

    - **Soporte experto**: Resuelve problemas postventa y desafíos técnicos con la ayuda de nuestra comunidad y equipo.
    - **Aprender y compartir**: Intercambia consejos y tutoriales para mejorar tus habilidades.
    - **Previsualizaciones exclusivas**: Obtén acceso temprano a anuncios de nuevos productos y adelantos exclusivos.
    - **Descuentos especiales**: Disfruta de descuentos exclusivos en nuestros productos más nuevos.
    - **Promociones y sorteos festivos**: Participa en sorteos y promociones festivas.

    👉 ¿Listo para explorar y crear con nosotros? Haz clic en [|link_sf_facebook|] y únete hoy mismo.


.. _remote_desktop:

Escritorio Remoto
======================

Puedes acceder y controlar el escritorio de la Raspberry Pi de forma remota desde otra computadora.  
El método recomendado es **VNC**, que está soportado oficialmente en Raspberry Pi OS y proporciona una experiencia de escritorio confiable y consistente.

La siguiente sección explica cómo habilitar VNC en tu Raspberry Pi y conectarte usando |shared_link_realvnc|.

-----------------

Habilitar el Servicio VNC
-------------------------

RealVNC Server viene preinstalado en Raspberry Pi OS, pero está **deshabilitado por defecto**.  
Debes habilitarlo mediante la herramienta de configuración.

#. Abre una terminal en tu computadora (Windows: **PowerShell**; macOS/Linux: **Terminal**) y conéctate a tu Raspberry Pi:

   .. code-block:: bash

      ssh <username>@<hostname>.local

   o

   .. code-block:: bash

      ssh <username>@<ip_address>

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



Iniciar sesión con RealVNC® Viewer
----------------------------------

#. Descarga e instala |shared_link_realvnc| según tu sistema operativo.

   .. image:: /_shared/appendix/img/ssh_vnc_download.png


#. Abre **RealVNC Viewer**, luego ingresa la dirección IP de tu Raspberry Pi o ``<hostname>.local`` y presiona **Enter**.

   .. image:: /_shared/appendix/img/ssh_vnc_login.png


#. Ingresa el **nombre de usuario** y **contraseña** de tu Raspberry Pi, luego selecciona **OK**.

   .. note::

      Al conectarte por primera vez, puede aparecer un mensaje como “VNC Server not recognized”. Selecciona **Continue** para proceder.

   .. image:: /_shared/appendix/img/ssh_vnc_username.png


#. Ahora deberías ver el escritorio de la Raspberry Pi:

   .. image:: /_shared/appendix/img/ssh_vnc_desktop.png


Esto completa el proceso de configuración de VNC.

-----------------

Notas Adicionales
-----------------

* **Se requiere la versión Desktop**

  * VNC necesita que la Raspberry Pi esté ejecutando la versión completa con escritorio de Raspberry Pi OS.  
  * Si usas **Raspberry Pi OS Lite**, instala VNC Server manualmente: ``sudo apt install realvnc-vnc-server``


* **Consejos para el rendimiento de red** 

  * Si experimentas lentitud o baja tasa de refresco, revisa la calidad de tu red.  
  * Ethernet por cable generalmente ofrece el mejor rendimiento.


* **Corrección de problemas de resolución**

  * Si la ventana VNC aparece demasiado pequeña o con resolución incorrecta, configura una resolución fija en: ``sudo raspi-config`` → **Display Options** → **VNC Resolution**


* **Asegúrate de que VNC esté habilitado**

  Si VNC no se conecta, verifica que esté habilitado en: ``sudo raspi-config`` → ``Interfacing Options`` → ``VNC``

* **Detener el servicio VNC**

  Para detener manualmente VNC Server: ``sudo systemctl stop vncserver-x11-serviced``


* **Recordatorio de seguridad**

  * VNC está diseñado para redes locales de confianza.  
  * **No** expongas VNC directamente a internet.  
  * Para acceso remoto seguro desde fuera de tu red, utiliza **Raspberry Pi Connect** o una VPN.
