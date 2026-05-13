.. note::

    ¡Hola, bienvenido a la comunidad de entusiastas de SunFounder Raspberry Pi & Arduino & ESP32 en Facebook! Sumérgete más en Raspberry Pi, Arduino y ESP32 con otros entusiastas.

    **¿Por qué unirse?**

    - **Soporte experto**: Resuelve problemas postventa y desafíos técnicos con la ayuda de nuestra comunidad y equipo.
    - **Aprender y compartir**: Intercambia consejos y tutoriales para mejorar tus habilidades.
    - **Previsualizaciones exclusivas**: Obtén acceso temprano a anuncios de nuevos productos y adelantos exclusivos.
    - **Descuentos especiales**: Disfruta de descuentos exclusivos en nuestros productos más nuevos.
    - **Promociones y sorteos festivos**: Participa en sorteos y promociones festivas.

    👉 ¿Listo para explorar y crear con nosotros? Haz clic en [|link_sf_facebook|] y únete hoy mismo.

.. _cpn_fusion_hat:

Fusion HAT+
=====================================

.. image:: img/fusionhat_v0.png
    :width: 500
    :align: center


La Fusion HAT+ es una placa de expansión potente y versátil diseñada para transformar fácilmente una Raspberry Pi en un robot completamente funcional con una configuración mínima, y también puede soportar proyectos de automatización avanzados.

En el corazón de la Fusion HAT+ se encuentra un microcontrolador (MCU) integrado, que amplía significativamente la funcionalidad nativa de la Raspberry Pi al proporcionar salidas PWM adicionales y entradas ADC, capacidades que normalmente están ausentes en los modelos estándar de Raspberry Pi. Esto permite a los desarrolladores lograr un control de motores y una integración de sensores más precisos.

Compacta en tamaño pero rica en funcionalidad, la Fusion HAT+ integra cuatro chips controladores de motor, que admiten el control independiente de hasta cuatro motores DC. También cuenta con un módulo de audio digital I2S y un altavoz mono integrado, lo que permite una reproducción de audio de alta calidad y funciones de sonido interactivas directamente desde la placa.

La placa acepta una entrada de alimentación de 6,0 V a 8,4 V a través de un conector XH2.54 de 3 pines. Incluye dos LED indicadores de alimentación para monitorear el estado del sistema, un LED programable por el usuario para señalización personalizada y un práctico botón integrado para pruebas de función inmediatas o simulación de entrada, lo que hace que el desarrollo y la depuración sean más eficientes y fáciles de usar.

.. |link_fusion_hat| raw:: html

    <a href="https://docs.sunfounder.com/projects/fusion-hat/en/latest/" target="_blank">SunFounder Fusion HAT+</a>

Para instrucciones detalladas, consulta: |link_fusion_hat|.

PinPal
============================

.. image:: img/pinpal_pic.png
    :width: 20%
    :align: center

PinPal es una pequeña placa PCB diseñada por SunFounder con etiquetas de pines del Raspberry Pi.
Puedes colocarla directamente sobre el conector de pines de la Fusion HAT+, lo que facilita identificar la función de cada pin de forma clara y rápida mientras construyes tu proyecto.
Esto ayuda a reducir errores y acelerar el cableado.

.. image:: img/pinpal_fusion_hat.png
    :width: 80%
    :align: center

Algunos pines en PinPal **no se recomiendan para uso directo** porque ya son utilizados por la Fusion HAT+ o comparten funciones que pueden causar conflictos.


#. **SDA / SCL — I2C (GPIO2 / GPIO3)**

   * Pines I2C principales de la Raspberry Pi.
   * La Fusion HAT+ también proporciona un conector I2C P2.54 y un puerto SH1.0 Qwiic/STEMMA QT.
   * Los tres comparten el mismo bus, por lo que **solo se puede usar uno a la vez**.

   .. image:: img/pinpal_i2c.png
       :width: 80%
       :align: center

#. **TXD / RXD — UART (GPIO14 / GPIO15)**

   * Pines UART principales de la Raspberry Pi.
   * La Fusion HAT+ incluye otro conector UART, compartiendo los mismos pines — **elige solo uno**.

   .. image:: img/pinpal_uart.png
       :width: 80%
       :align: center

#. **GPIO 17 / 4 / 27 / 22 — GPIO Generales**

   * La Fusion HAT+ proporciona un conjunto adicional de estos pines, pero corresponden a los mismos GPIO de la Raspberry Pi.
   * **Usa solo un grupo** para evitar conflictos.

   .. image:: img/pinpal_gpio.png
       :width: 80%
       :align: center

#. **MOSI / MISO / SCLK / CE0 / GPIO6 — Pines SPI**

   * La Fusion HAT+ proporciona otro conector SPI.
   * El conector RGB (WS2812) usa el pin MOSI.
   * **Usa solo un grupo SPI** para evitar conflictos.


   .. list-table::
      :header-rows: 1

      * - Señal
        - Mapeo de Pines
      * - BSY
        - GPIO6
      * - CS
        - CE0 / GPIO8
      * - SCK
        - SCLK / GPIO11
      * - MI
        - MISO / GPIO9
      * - MO
        - MOSI / GPIO10

   .. image:: img/pinpal_spi.png
       :width: 80%
       :align: center


#. **GPIO 18 / 19 / 20 / 21 — Pines de Audio I2S**

   * La Fusion HAT+ incluye audio I2S integrado (altavoz + micrófono). Más detalles:
     `I2S <https://docs.sunfounder.com/projects/fusion-hat/en/latest/hardware/interfaces.html#speaker-and-mic>`_.
   * Puedes reutilizar estos pines solo cuando el sistema de audio esté apagado.
   * **No uses WS ni SCLK mientras los componentes de audio estén activos.**

   .. image:: img/pinpal_i2s.png
       :width: 80%
       :align: center

   .. list-table::
      :header-rows: 1

      * - Señal
        - Pin Raspberry Pi
      * - WS
        - GPIO19
      * - SCLK
        - GPIO18
      * - Salida de Audio (Altavoz)
        - GPIO21
      * - Entrada de Audio (MIC)
        - GPIO20


#. **ID_SD / ID_SC — Pines EEPROM del HAT**

   Estos pines están reservados para el EEPROM del HAT de Raspberry Pi, que almacena datos de identificación de la placa.
   La Fusion HAT+ usa estos pines para su EEPROM integrado, por lo que **ID_SD (GPIO0) e ID_SC (GPIO1) no deben usarse para ningún otro propósito**.


   .. image:: img/pinpal_eeprom.png
       :width: 80%
       :align: center

