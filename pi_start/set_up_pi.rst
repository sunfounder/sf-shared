.. note::

    ¡Hola, bienvenido a la comunidad de entusiastas de SunFounder Raspberry Pi & Arduino & ESP32 en Facebook! Sumérgete más en Raspberry Pi, Arduino y ESP32 con otros entusiastas.

    **¿Por qué unirse?**

    - **Soporte experto**: Resuelve problemas postventa y desafíos técnicos con la ayuda de nuestra comunidad y equipo.
    - **Aprender y compartir**: Intercambia consejos y tutoriales para mejorar tus habilidades.
    - **Previsualizaciones exclusivas**: Obtén acceso temprano a anuncios de nuevos productos y adelantos exclusivos.
    - **Descuentos especiales**: Disfruta de descuentos exclusivos en nuestros productos más nuevos.
    - **Promociones y sorteos festivos**: Participa en sorteos y promociones festivas.

    👉 ¿Listo para explorar y crear con nosotros? Haz clic en [|link_sf_facebook|] y únete hoy mismo.

.. _setup_pi:

Configura tu Raspberry Pi
==================================

Para comenzar a programar y controlar tu Raspberry Pi, primero necesitas acceder a ella.  
Esta guía describe dos métodos comunes:

* Usar un monitor, teclado y ratón  
* Configurar una conexión sin pantalla (headless) para acceso remoto  

.. note::

   La Raspberry Pi Zero 2W instalada en el robot no es fácil de conectar a una pantalla.  
   Recomendamos usar el método de **configuración headless**.

-------------------------
Si Tienes Pantalla
-------------------------

**Componentes Necesarios**

* Raspberry Pi
* Fuente de Alimentación Oficial
* Tarjeta MicroSD
* Cable HDMI  
  (Para Raspberry Pi 4/5, usa **HDMI0**, el puerto más cercano al conector de alimentación.)
* Monitor
* Teclado y Ratón

**Pasos**

#. Inserta la tarjeta microSD en tu Raspberry Pi.
#. Conecta el teclado, el ratón y el monitor.
#. Enciende tu Raspberry Pi.
#. Después de iniciar, aparecerá el escritorio del sistema operativo Raspberry Pi. 

   .. image:: /_shared/pi_start/img/plug_screen_trixie.png
      :width: 80%
      :align: center

#. Abre una **Terminal** para introducir comandos.

   .. image:: /_shared/pi_start/img/open_terminal.png
      :width: 80%
      :align: center


----------------------------------
Si No Tienes Pantalla (Headless)
----------------------------------

Sin un monitor, puedes configurar e iniciar sesión en tu Raspberry Pi de forma remota.  
Este es el método más conveniente para la mayoría de los usuarios.

**Componentes Necesarios**

* Raspberry Pi
* Fuente de Alimentación Oficial
* Tarjeta MicroSD
* Un ordenador en la misma red

**Consejos**

* Asegúrate de haber completado todas las configuraciones descritas en :ref:`imager_custom` al instalar el sistema con Raspberry Pi Imager.
* Asegúrate de que tu Raspberry Pi y tu ordenador estén en la misma red local.
* Para mayor estabilidad, usa Ethernet si está disponible.


**Conectarse vía SSH**

#. Abre una terminal en tu ordenador (Windows: **PowerShell**; macOS/Linux: **Terminal**) y conéctate a tu Raspberry Pi:

   .. code-block:: bash

      ssh <usuario>@<hostname>.local
      # Ejemplo:
      ssh daisy@pi.local

2. Alternativamente, localiza la dirección IP de tu Pi desde la lista DHCP de tu router y conéctate con:

   .. code-block:: bash

      ssh <usuario>@<dirección IP>
      # Ejemplo:
      ssh daisy@192.168.1.42

3. En el primer inicio de sesión, escribe ``yes`` para confirmar el certificado SSH.

4. Introduce la contraseña que configuraste en Raspberry Pi Imager.  
   (No aparecerá nada mientras escribes—esto es normal.)

5. Después de iniciar sesión, tendrás acceso completo a la línea de comandos.

   .. image:: /_shared/pi_start/img/ssh_login.png
      :align: center

----------------------

**Solución de Problemas**

* **ssh: Could not resolve hostname ...**

  * Asegúrate de que el nombre del host sea correcto.
  * Intenta conectarte usando la dirección IP de la Pi.

* **The term 'ssh' is not recognized... (Windows)**

  * OpenSSH no está instalado. Instálalo manualmente o usa un cliente SSH de terceros.  
  * Consulta :ref:`openssh_powershell` o :ref:`login_windows`.

* **Permission denied (publickey,password)**

  * Asegúrate de usar el nombre de usuario y la contraseña creados en Raspberry Pi Imager.

* **Connection refused**

  * Espera 1–2 minutos después de encender.
  * Confirma que SSH esté habilitado en Raspberry Pi Imager.

--------------------------------

Opciones de Acceso Gráfico Remoto
-------------------------------------

.. |shared_link_rpi_connect| raw:: html

    <a href="https://www.raspberrypi.com/documentation/services/connect.html" target="_blank">Raspberry Pi Connect</a> 

Si prefieres una interfaz gráfica:

* :ref:`remote_desktop`: Habilita **VNC (Virtual Network Computing)** para una experiencia de escritorio completa en tu Pi.

* |shared_link_rpi_connect|: Usa Raspberry Pi Connect para acceso remoto seguro desde cualquier lugar, directamente en un navegador. 

Ahora puedes controlar tu Raspberry Pi sin un monitor, ya sea mediante SSH para operaciones en la línea de comandos, o con VNC / Raspberry Pi Connect para una experiencia de escritorio gráfica.
