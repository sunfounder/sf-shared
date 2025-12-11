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

Instalación del Sistema Operativo
===================================

.. start_imager

Antes de usar tu Raspberry Pi, necesitas instalar **Raspberry Pi OS** en una tarjeta microSD.  
Esta guía explica cómo hacerlo usando **Raspberry Pi Imager** de una forma sencilla y apta para principiantes.

**Componentes Necesarios**

* Una computadora (Windows, macOS o Linux)
* Una tarjeta microSD (16 GB o más; marcas recomendadas: SanDisk, Samsung)
* Un lector de tarjetas microSD

-------------------

**1. Instalar Raspberry Pi Imager**
-------------------------------------------

#. Visita la página oficial de descarga de Raspberry Pi Imager: |shared_link_rpi_imager|. Descarga el instalador adecuado para tu sistema operativo.

   .. image:: /_shared/pi_start/img/imager_download.png
      :width: 70%

#. Sigue las indicaciones de instalación (idioma, ruta de instalación, confirmación). Tras la instalación, inicia **Raspberry Pi Imager** desde tu escritorio o menú de aplicaciones.

   .. image:: /_shared/pi_start/img/imager_install.png
      :width: 90%

-------------------

**2. Instalar el Sistema Operativo en la Tarjeta microSD**
-----------------------------------------------------------

#. Inserta la tarjeta microSD en tu computadora usando un lector de tarjetas. Haz copia de seguridad de cualquier dato importante antes de continuar.

   .. image:: /_shared/pi_start/img/insert_sd.png
      :width: 90%

#. Cuando Raspberry Pi Imager se abra, verás la página **Device (Dispositivo)**. Selecciona el modelo de tu Raspberry Pi (por ejemplo, Raspberry Pi 5, 4, 3 o Zero 2W).

   .. image:: /_shared/pi_start/img/imager_device.png
      :width: 90%

   .. end_imager

#. Ve a la sección **OS** y elige la opción recomendada **Raspberry Pi OS (64-bit)**.

   .. image:: /_shared/pi_start/img/imager_os.png
      :width: 90%

   .. start_choose_os

#. En la sección **Storage**, selecciona tu tarjeta microSD. Para evitar errores, desconecta otras unidades USB para que solo aparezca la tarjeta SD.

   .. image:: /_shared/pi_start/img/imager_storage.png
      :width: 90%

#. Haz clic en **Next** para continuar a la configuración avanzada.

   .. note::

      * Si conectarás monitor, teclado y ratón directamente a tu Raspberry Pi, puedes hacer clic en **SKIP CUSTOMISATION**.  
      * Si planeas configurar la Raspberry Pi *sin monitor* (acceso remoto por Wi-Fi), debes completar la configuración avanzada.

   .. image:: /_shared/pi_start/img/imager_custom_skip.png
      :width: 90%

-------------------

.. _imager_custom:

**3. Configuración Avanzada del Sistema Operativo**
---------------------------------------------------

#. **Configurar Hostname**

   * Asigna un nombre único para tu Raspberry Pi.  
   * Luego podrás conectarte usando ``hostname.local``.

   .. image:: /_shared/pi_start/img/imager_custom_hostname.png
      :width: 90%

#. **Configurar Localización**

   * Selecciona tu ciudad capital.
   * Imager completará automáticamente la zona horaria y el diseño del teclado, aunque puedes ajustarlos si es necesario. Selecciona Next.
   
   .. image:: /_shared/pi_start/img/imager_custom_local.png
      :width: 90%

#. **Configurar Usuario y Contraseña**

   Crea una cuenta de usuario para tu Raspberry Pi.
   
   .. image:: /_shared/pi_start/img/imager_custom_user.png
      :width: 90%

#. **Configurar Wi-Fi**

   * Ingresa el **SSID** (nombre de red) y la **contraseña** de tu Wi-Fi.  
   * Tu Raspberry Pi se conectará automáticamente al iniciar.
   
   .. image:: /_shared/pi_start/img/imager_custom_wifi.png
      :width: 90%

#. **Habilitar SSH (Opcional pero Recomendado)**

   * SSH te permite iniciar sesión de manera remota desde tu computadora.  
   * Puedes iniciar sesión usando usuario/contraseña o configurar claves SSH.
   
   .. image:: /_shared/pi_start/img/imager_custom_ssh.png
      :width: 90%

#. **Habilitar Raspberry Pi Connect (Opcional)**

   Raspberry Pi Connect permite acceder al escritorio de tu Raspberry Pi desde un navegador web.
   
   * Activa **Raspberry Pi Connect**, luego haz clic en **OPEN RASPBERRY PI CONNECT**.
   
     .. image:: /_shared/pi_start/img/imager_custom_connect.png
        :width: 90%

   * Se abrirá la página web de Raspberry Pi Connect en tu navegador. Inicia sesión con tu cuenta de Raspberry Pi ID o regístrate si aún no tienes una.

     .. image:: /_shared/pi_start/img/imager_custom_open.png
        :width: 90%

   * En la página **New auth key**, crea tu clave de autenticación temporal.
      
      * Si tu cuenta no pertenece a ninguna organización, selecciona **Create auth key and launch Raspberry Pi Imager**.  
      * Si perteneces a una o más organizaciones, elige una, luego genera la clave y abre Imager.  
      * Asegúrate de encender tu Raspberry Pi y conectarla a internet antes de que la clave caduque.
   
     .. image:: /_shared/pi_start/img/imager_custom_authkey.png
        :width: 90%
   
   * Tu navegador puede pedir permiso para abrir Raspberry Pi Imager — permítelo.

     * Imager se abrirá en la pestaña Raspberry Pi Connect mostrando el token de autenticación.  
     * Si el token no se transfiere automáticamente, abre la sección **Having trouble?** en la página de Raspberry Pi Connect, copia el token y pégalo manualmente en Imager.

     .. image:: /_shared/pi_start/img/imager_custom_connect_token.png
        :width: 90%

-------------------

**4. Escribir la Imagen del Sistema Operativo**
-----------------------------------------------

#. Revisa toda la configuración y haz clic en **WRITE**.

   .. image:: /_shared/pi_start/img/imager_writing.png
      :width: 90%

#. Si la tarjeta contiene datos, Raspberry Pi Imager mostrará una advertencia indicando que todos los datos se borrarán. Verifica que seleccionaste la unidad correcta, luego haz clic en **I UNDERSTAND, ERASE AND WRITE** para continuar.

   .. image:: /_shared/pi_start/img/imager_erase.png
      :width: 90%

#. Espera a que finalicen la escritura y verificación. Al completarse, Raspberry Pi Imager mostrará **Write complete!** junto con un resumen de tu configuración. La unidad será expulsada automáticamente para retirarla con seguridad.

   .. image:: /_shared/pi_start/img/imager_finish.png
        :width: 90%

#. Retira la tarjeta microSD e insértala en la ranura ubicada en la parte inferior de tu Raspberry Pi. ¡Tu Raspberry Pi está lista para arrancar con el nuevo sistema operativo!

   .. image:: /_shared/pi_start/img/os_sd_to_pi.jpg
        :width: 70%

   .. end_choose_os

