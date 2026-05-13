.. note::

    ¡Hola, bienvenido a la comunidad de entusiastas de SunFounder Raspberry Pi & Arduino & ESP32 en Facebook! Sumérgete más en Raspberry Pi, Arduino y ESP32 con otros entusiastas.

    **¿Por qué unirse?**

    - **Soporte experto**: Resuelve problemas postventa y desafíos técnicos con la ayuda de nuestra comunidad y equipo.
    - **Aprender y compartir**: Intercambia consejos y tutoriales para mejorar tus habilidades.
    - **Previsualizaciones exclusivas**: Obtén acceso temprano a anuncios de nuevos productos y adelantos exclusivos.
    - **Descuentos especiales**: Disfruta de descuentos exclusivos en nuestros productos más nuevos.
    - **Promociones y sorteos festivos**: Participa en sorteos y promociones festivas.

    👉 ¿Listo para explorar y crear con nosotros? Haz clic en [|link_sf_facebook|] y únete hoy mismo.

.. _cpn_oled:

Módulo de Pantalla OLED
==========================

.. image:: img/oled.png
    :width: 300
    :align: center

Introducción
---------------------------
Un módulo de pantalla OLED (Diodo Orgánico Emisor de Luz) es un dispositivo que puede mostrar texto, gráficos e imágenes en una pantalla delgada y flexible utilizando materiales orgánicos que emiten luz cuando se aplica corriente eléctrica.

La principal ventaja de una pantalla OLED es que emite su propia luz y no necesita otra fuente de retroiluminación. Debido a esto, las pantallas OLED suelen tener mejor contraste, brillo y ángulos de visión en comparación con las pantallas LCD.

Otra característica importante de las pantallas OLED son los niveles de negro profundo. Dado que cada píxel emite su propia luz en una pantalla OLED, para producir el color negro, el píxel individual se puede apagar.

Debido al menor consumo de energía (solo los píxeles encendidos consumen corriente), las pantallas OLED también son populares en dispositivos que funcionan con batería, como relojes inteligentes, rastreadores de salud y otros dispositivos portátiles.

Principio
---------------------------
Un módulo de pantalla OLED consta de un panel OLED y un chip controlador OLED montado en la parte posterior del módulo. El panel OLED está formado por muchos píxeles diminutos que pueden producir diferentes colores de luz. Cada píxel consta de varias capas de materiales orgánicos intercaladas entre dos electrodos (ánodo y cátodo). Cuando la corriente eléctrica fluye a través de los electrodos, los materiales orgánicos emiten luz de diferentes longitudes de onda según su composición.

El chip controlador OLED es un chip que puede controlar los píxeles del panel OLED utilizando un protocolo de comunicación serie llamado I2C (Circuito Inter-Integrado).

El chip controlador OLED convierte las señales del Arduino en comandos para el panel OLED. El Arduino puede enviar datos al chip controlador OLED utilizando una biblioteca que puede controlar el protocolo I2C. Una de estas bibliotecas es la biblioteca Adafruit SSD1306. Con esta biblioteca, puedes inicializar el módulo de pantalla OLED, establecer el nivel de brillo, imprimir texto, gráficos o imágenes, etc.

.. **Ejemplo**

.. * :ref:`basic_oled` (Proyecto Básico)
.. * :ref:`fun_pong` (Proyecto Divertido)
.. * :ref:`iot_weathertime_screen` (Proyecto IoT)
