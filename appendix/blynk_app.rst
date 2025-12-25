.. note::

    ¡Hola! Bienvenido a la comunidad de entusiastas de SunFounder Raspberry Pi, Arduino y ESP32 en Facebook. Sumérgete en el mundo de Raspberry Pi, Arduino y ESP32 con otros entusiastas.

    **¿Por qué unirse?**

    - **Soporte experto**: Resuelve problemas post-venta y desafíos técnicos con la ayuda de nuestra comunidad y equipo.
    - **Aprender y compartir**: Intercambia consejos y tutoriales para mejorar tus habilidades.
    - **Avances exclusivos**: Obtén acceso anticipado a nuevos anuncios de productos y adelantos.
    - **Descuentos especiales**: Disfruta de descuentos exclusivos en nuestros productos más nuevos.
    - **Promociones y sorteos festivos**: Participa en sorteos y promociones festivas.

    👉 ¿Listo para explorar y crear con nosotros? Haz clic en [|link_sf_facebook|] y únete hoy mismo!

.. _blynk_mobile:

¿Cómo usar Blynk en un dispositivo móvil?
===================================================

.. note::

    Como los flujos de datos (datastreams) solo pueden crearse en Blynk desde la web, necesitarás consultar distintos proyectos para crear los datastreams en la versión web y, luego, seguir el tutorial que aparece a continuación para crear los widgets en Blynk desde tu dispositivo móvil.


#. Abre Google Play o la App Store en tu dispositivo móvil y busca “Blynk IoT” (no Blynk (legacy)) para descargarlo.
#. Después de abrir la aplicación, inicia sesión. Esta cuenta debe ser la misma que usas en el cliente web.
#. Luego ve a **Dashboard** (si no tienes uno, crea uno) y verás que los **Dashboards** para móvil y web son independientes entre sí.

    .. image:: img/APP_1.jpg

#. Haz clic en el icono **Edit**.
#. Haz clic en un área en blanco.
#. Elige el mismo widget que en la página web, por ejemplo, selecciona el widget **Joystick**.

    .. image:: img/APP_2.jpg

#. Ahora verás que aparece un widget **Joystick** en el área en blanco; haz clic sobre él.
#. Aparecerán los ajustes del **Joystick**. Selecciona los datastreams **Xvalue** y **Yvalue** que configuraste previamente en la página web. Ten en cuenta que cada widget corresponde a un datastream diferente en cada proyecto.
#. Regresa a la página de **Dashboard** y ya podrás usar el **Joystick** cuando lo desees.

    .. image:: img/APP_3.jpg
