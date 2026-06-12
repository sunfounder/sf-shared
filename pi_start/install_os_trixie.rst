.. note::

    ¡Hola, bienvenido a la comunidad de entusiastas de SunFounder Raspberry Pi & Arduino & ESP32 en Facebook! Sumérgete más en Raspberry Pi, Arduino y ESP32 con otros entusiastas.

    **¿Por qué unirse?**

    - **Soporte experto**: Resuelve problemas postventa y desafíos técnicos con la ayuda de nuestra comunidad y equipo.
    - **Aprender y compartir**: Intercambia consejos y tutoriales para mejorar tus habilidades.
    - **Previsualizaciones exclusivas**: Obtén acceso temprano a anuncios de nuevos productos y adelantos exclusivos.
    - **Descuentos especiales**: Disfruta de descuentos exclusivos en nuestros productos más nuevos.
    - **Promociones y sorteos festivos**: Participa en sorteos y promociones festivas.

    👉 ¿Listo para explorar y crear con nosotros? Haz clic en [|link_sf_facebook|] y únete hoy mismo.

.. _install_os:

Instalación del sistema operativo
===================================

.. start_imager

Antes de usar tu Raspberry Pi, necesitas instalar **Raspberry Pi OS** en una tarjeta microSD.
Esta guía explica cómo hacerlo usando **Raspberry Pi Imager** de una manera sencilla y apta para principiantes.

**Componentes necesarios**

* Un ordenador (Windows, macOS o Linux)
* Una tarjeta microSD (16 GB o más; marcas recomendadas: SanDisk, Samsung)
* Un lector de tarjetas microSD

-------------------

Instalar Raspberry Pi Imager
-------------------------------------------

.. |shared_link_rpi_imager| raw:: html

    <a href="https://www.raspberrypi.com/software/" target="_blank">Raspberry Pi Imager</a>

#. Visita la página oficial de descarga de Raspberry Pi Imager: |shared_link_rpi_imager|. Descarga el instalador correspondiente a tu sistema operativo.

   .. image:: /_shared/pi_start/img/imager_download.png
      :width: 70%

#. Sigue los pasos de instalación (idioma, ruta de instalación, confirmación). Una vez finalizada la instalación, inicia **Raspberry Pi Imager** desde el escritorio o el menú de aplicaciones.

   .. image:: /_shared/pi_start/img/imager_install.png
      :width: 90%

--------------------------------------

.. end_imager


.. start_install_os

Instalar el sistema operativo en la tarjeta microSD
-----------------------------------------------------

1. Inserta la tarjeta microSD en tu ordenador usando un lector de tarjetas. Haz una copia de seguridad de cualquier dato importante antes de continuar.

   .. image:: /_shared/pi_start/img/insert_sd.png
      :width: 90%

2. Cuando se abra Raspberry Pi Imager, verás la página **Device**. Selecciona tu modelo de Raspberry Pi en la lista (por ejemplo, Raspberry Pi 5, 4, 3 o Zero 2W).

   .. image:: /_shared/pi_start/img/imager_device.png
      :width: 90%

.. end_install_os

3. Ve a la sección **OS** y elige la opción recomendada **Raspberry Pi OS (64-bit)**.

   .. image:: /_shared/pi_start/img/imager_os.png
      :width: 90%

   .. tip::
      No instale la versión de 32 bits, ya que algunas dependencias necesarias podrían no estar disponibles.

.. start_storage

4. En la sección **Storage**, selecciona tu tarjeta microSD.

   .. image:: /_shared/pi_start/img/imager_storage.png
      :width: 90%

.. end_storage

-------------------

.. start_cutomization_os

.. _imager_custom:

Ajustes de personalización del sistema operativo
--------------------------------------------------

#. Continúa con el paso de personalización.

   * Si vas a conectar un monitor, teclado y ratón directamente a tu Raspberry Pi, puedes hacer clic en **SKIP CUSTOMISATION**.
   * Si planeas configurar la Raspberry Pi en modo *headless* (acceso remoto por Wi-Fi), debes completar los ajustes de personalización.

   .. image:: /_shared/pi_start/img/imager_custom_skip.png
      :width: 90%

#. **Configurar el nombre de host**

   * Asigna un nombre de host único a tu Raspberry Pi.
   * Podrás conectarte más adelante usando ``hostname.local``.

   .. image:: /_shared/pi_start/img/imager_custom_hostname.png
      :width: 90%

#. **Configurar la localización**

   * Elige tu ciudad capital.
   * Imager completará automáticamente la zona horaria y la distribución del teclado según tu selección, aunque puedes ajustarlas si es necesario. Selecciona Next.

   .. image:: /_shared/pi_start/img/imager_custom_local.png
      :width: 90%

#. **Configurar usuario y contraseña**

   Crea una cuenta de usuario para tu Raspberry Pi.

   .. image:: /_shared/pi_start/img/imager_custom_user.png
      :width: 90%

#. **Configurar Wi-Fi**

   * Introduce el **SSID** (nombre de la red) y la **contraseña** de tu Wi-Fi.
   * Tu Raspberry Pi se conectará automáticamente en el primer arranque.

   .. image:: /_shared/pi_start/img/imager_custom_wifi.png
      :width: 90%

#. **Habilitar SSH (opcional pero recomendado)**

   * Habilitar SSH te permite iniciar sesión de forma remota desde tu ordenador.
   * Puedes iniciar sesión con tu usuario/contraseña o configurar claves SSH.

   .. image:: /_shared/pi_start/img/imager_custom_ssh.png
      :width: 90%

.. end_cutomization_os

.. start_enable_connection

#. **Habilitar Raspberry Pi Connect (opcional)**

   Raspberry Pi Connect te permite acceder al escritorio de tu Raspberry Pi desde un navegador web.

   * Activa **Raspberry Pi Connect** y luego haz clic en **OPEN RASPBERRY PI CONNECT**.

     .. image:: /_shared/pi_start/img/imager_custom_connect.png
        :width: 90%

   * El sitio web de Raspberry Pi Connect se abrirá en tu navegador predeterminado. Inicia sesión con tu cuenta de Raspberry Pi ID o regístrate si aún no tienes una.

     .. image:: /_shared/pi_start/img/imager_custom_open.png
        :width: 90%

   * En la página **New auth key**, crea tu clave de autenticación de un solo uso.

      * Si tu cuenta de Raspberry Pi ID no pertenece a ninguna organización, selecciona **Create auth key and launch Raspberry Pi Imager**.
      * Si perteneces a una o más organizaciones, elige una y luego crea la clave y abre Imager.
      * Asegúrate de encender tu Raspberry Pi y conectarla a Internet antes de que la clave caduque.

     .. image:: /_shared/pi_start/img/imager_custom_authkey.png
        :width: 90%

   * Tu navegador puede pedirte permiso para abrir Raspberry Pi Imager; acéptalo.

     * Imager se abrirá en la pestaña de Raspberry Pi Connect y mostrará el token de autenticación.
     * Si el token no se transfiere automáticamente, abre la sección **Having trouble?** en la página de Raspberry Pi Connect, copia el token y pégalo manualmente en Imager.

     .. image:: /_shared/pi_start/img/imager_custom_connect_token.png
        :width: 90%

.. end_enable_connection

-------------------

.. start_write_os

Escribir la imagen del sistema operativo
------------------------------------------


#. Revisa todos los ajustes y haz clic en **WRITE**.

   .. image:: /_shared/pi_start/img/imager_writing.png
      :width: 90%

#. Si la tarjeta ya contiene datos, Raspberry Pi Imager mostrará una advertencia indicando que todos los datos del dispositivo se borrarán. Verifica que has seleccionado la unidad correcta y haz clic en **I UNDERSTAND, ERASE AND WRITE** para continuar.

   .. image:: /_shared/pi_start/img/imager_erase.png
      :width: 90%

#. Espera a que finalicen la escritura y la verificación. Cuando termine, Raspberry Pi Imager mostrará **Write complete!** y un resumen de tus opciones. El dispositivo de almacenamiento se expulsará automáticamente para que puedas retirarlo de forma segura.


   .. image:: /_shared/pi_start/img/imager_finish.png
        :width: 90%

#. Retira la tarjeta microSD e insértala en la ranura situada en la parte inferior de tu Raspberry Pi. ¡Tu Raspberry Pi ya está lista para arrancar con el nuevo sistema operativo!

   .. image:: /_shared/pi_start/img/os_sd_to_pi.jpg
        :width: 70%

.. end_write_os
