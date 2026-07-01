.. note::

    ¡Hola, bienvenido a la comunidad de entusiastas de SunFounder Raspberry Pi, Arduino y ESP32 en Facebook! Sumérgete más profundamente en Raspberry Pi, Arduino y ESP32 con otros entusiastas.

    **¿Por qué unirse?**

    - **Soporte experto**: Resuelve problemas postventa y desafíos técnicos con la ayuda de nuestra comunidad y equipo.
    - **Aprende y comparte**: Intercambia consejos y tutoriales para mejorar tus habilidades.
    - **Vistas previas exclusivas**: Obtén acceso anticipado a anuncios de nuevos productos y avances.
    - **Descuentos especiales**: Disfruta de descuentos exclusivos en nuestros productos más recientes.
    - **Promociones festivas y sorteos**: Participa en sorteos y promociones de temporada.

    👉 ¿Listo para explorar y crear con nosotros? Haz clic en [|link_sf_facebook|] y únete hoy mismo.

.. _cpn_ultrasonic_sensor:

Módulo Ultrasónico
================================

.. image:: /_shared/component/img/ultrasonic_pic.png
    :width: 400
    :align: center

El módulo de medición ultrasónica proporciona una función de medición sin contacto de 2 cm a 400 cm, y la precisión de la medición puede alcanzar los 3 mm.
Puede garantizar que la señal sea estable dentro de los 5 m, y la señal se debilita gradualmente después de los 5 m, hasta que desaparece en la posición de 7 m.

El módulo incluye transmisores ultrasónicos, receptor y circuito de control. Los principios básicos son los siguientes:

#. Use un flip-flop de IO para procesar una señal de alto nivel de al menos 10 us.

#. El módulo envía automáticamente ocho pulsos de 40 kHz y detecta si hay una señal de pulso de retorno.

#. Si la señal regresa, pasando el nivel alto, la duración de salida alta del IO es el tiempo desde la transmisión de la onda ultrasónica hasta su retorno. Aquí, la distancia de prueba = (tiempo alto x velocidad del sonido (340 m / s) / 2).

El diagrama de tiempos se muestra a continuación.

.. image:: /_shared/component/img/ultrasonic228.png

Solo necesitas suministrar un pulso corto de 10 us para que la entrada del trigger 
inicie la medición, y luego el módulo enviará una ráfaga de 8 ciclos de ultrasonido 
a 40 kHz y elevará su eco. Puedes calcular la distancia a través del intervalo de 
tiempo entre el envío de la señal de disparo y la recepción de la señal de eco.

Fórmula: us / 58 = centímetros o us / 148 = pulgadas; o: la distancia = tiempo de alto 
nivel \* velocidad (340M/S) / 2; se sugiere usar un ciclo de medición superior a 60 ms 
para evitar colisiones de señal entre la señal de disparo y la señal de eco.

.. **Ejemplo**

.. * :ref:`2.2.8_c` (C Project)
.. * :ref:`3.1.3_c` (C Project)
.. * :ref:`2.2.8_py` (Python Project)
.. * :ref:`4.1.9_py` (Python Project)
