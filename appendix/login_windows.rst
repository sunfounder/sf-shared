.. note::

    ¡Hola! Bienvenido a la comunidad de entusiastas de SunFounder Raspberry Pi, Arduino y ESP32 en Facebook. Sumérgete en el mundo de Raspberry Pi, Arduino y ESP32 con otros entusiastas.

    **¿Por qué unirse?**

    - **Soporte experto**: Resuelve problemas post-venta y desafíos técnicos con la ayuda de nuestra comunidad y equipo.
    - **Aprender y compartir**: Intercambia consejos y tutoriales para mejorar tus habilidades.
    - **Avances exclusivos**: Obtén acceso anticipado a nuevos anuncios de productos y adelantos.
    - **Descuentos especiales**: Disfruta de descuentos exclusivos en nuestros productos más nuevos.
    - **Promociones y sorteos festivos**: Participa en sorteos y promociones festivas.

    👉 ¿Listo para explorar y crear con nosotros? Haz clic en [|link_sf_facebook|] y únete hoy mismo!

.. _login_windows:

PuTTY
=========================

PuTTY es un cliente SSH sencillo y fiable para usuarios de Windows que permite acceder de forma remota a la Raspberry Pi.  


.. |shared_link_putty| raw:: html

    <a href="https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html" target="_blank">PuTTY</a> 


#. Descarga PuTTY desde |shared_link_putty| e instálalo en tu computadora.

   .. image:: /_shared/appendix/img/putty_download.png
      :width: 70%


#. Abre PuTTY y prepara la conexión:

   * Introduce el **hostname o la dirección IP** de tu Raspberry Pi en **Host Name**.
   * Configura el **Port** en ``22``.
   * Haz clic en **Open** para conectarte.


   .. image:: /_shared/appendix/img/putty_open.png
      :width: 70%
   
#. Si aparece una advertencia de seguridad en el primer uso, haz clic en **Accept** para continuar.

   .. image:: /_shared/appendix/img/putty_accept.png
      :width: 70%

#. Inicia sesión en la Raspberry Pi:

   * Cuando veas **login as:**, introduce el nombre de usuario que configuraste en **Raspberry Pi Imager**.
   * Introduce tu contraseña (no aparecerá mientras escribes; esto es normal).
   * Después de iniciar sesión, la terminal estará lista para que introduzcas comandos y operes tu Raspberry Pi de forma remota.

   .. image:: /_shared/appendix/img/putty_login.png
      :width: 70%

.. note::

    Si PuTTY muestra **inactive**, la conexión se ha perdido y es necesario volver a conectarse.
