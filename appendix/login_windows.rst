.. note::

    ¡Hola, bienvenido a la comunidad de entusiastas de SunFounder Raspberry Pi & Arduino & ESP32 en Facebook! Sumérgete más en Raspberry Pi, Arduino y ESP32 con otros entusiastas.

    **¿Por qué unirse?**

    - **Soporte experto**: Resuelve problemas postventa y desafíos técnicos con la ayuda de nuestra comunidad y equipo.
    - **Aprender y compartir**: Intercambia consejos y tutoriales para mejorar tus habilidades.
    - **Previsualizaciones exclusivas**: Obtén acceso temprano a anuncios de nuevos productos y adelantos exclusivos.
    - **Descuentos especiales**: Disfruta de descuentos exclusivos en nuestros productos más nuevos.
    - **Promociones y sorteos festivos**: Participa en sorteos y promociones festivas.

    👉 ¿Listo para explorar y crear con nosotros? Haz clic en [|link_sf_facebook|] y únete hoy mismo.

.. _login_windows:

PuTTY
=========================

PuTTY es un cliente SSH simple y confiable para que los usuarios de Windows accedan remotamente a la Raspberry Pi.

#. Descarga PuTTY desde |shared_link_putty| e instálalo en tu computadora.

   .. image:: /_shared/appendix/img/putty_download.png
      :width: 70%


#. Abre PuTTY y prepara la conexión:

   * Ingresa el **nombre de host (hostname) o dirección IP** de tu Raspberry Pi en **Host Name**.
   * Configura el **Puerto** en ``22``.
   * Haz clic en **Open** para conectar.


   .. image:: /_shared/appendix/img/putty_open.png
      :width: 70%
   
#. Si aparece una advertencia de seguridad en el primer uso, haz clic en **Accept** para continuar.

   .. image:: /_shared/appendix/img/putty_accept.png
      :width: 70%

#. Inicia sesión en la Raspberry Pi:

   * Cuando aparezca **login as:**, escribe el nombre de usuario configurado en **Raspberry Pi Imager**.
   * Ingresa tu contraseña (no se mostrará mientras escribes—esto es normal).
   * Después de iniciar sesión, el terminal estará listo para que ingreses comandos y operes tu Raspberry Pi de forma remota.

   .. image:: /_shared/appendix/img/putty_login.png
      :width: 70%

.. note::

    Si PuTTY muestra **inactive**, la conexión se perdió y será necesario reconectarse.
