.. _cpn_circular_ws2812_module:

Módulo LED WS2812 Circular
===========================================================

.. image:: img/c_ws2812_module.png
    :width: 40%
    :align: center

Este módulo LED WS2812 circular contiene 12 LED RGB direccionables individualmente, cada uno con un controlador integrado que admite un control de color de 24 bits a través de una sola línea de datos. El módulo expone cuatro pines — VCC, GND, DIN y DOUT — para una fácil conexión a controladores como Raspberry Pi o Arduino.

**Descripción de los Pines**

* **V (VCC)**: Entrada de alimentación de 5 V. Asegúrate de que tu fuente de alimentación pueda proporcionar suficiente corriente para todos los LED.
* **G (GND)**: Tierra. Debe ser compartida con tu controlador para una correcta señalización.
* **R (DIN)**: Recibe datos de tu microcontrolador. Es la entrada de control.
* **D (DOUT)**: Envía datos a anillos o tiras LED adicionales, permitiendo la expansión en cadena.

**Uso**

Los LED se pasan los datos de uno a otro, permitiendo el control independiente de cada LED y posibilitando efectos como barridos de color, degradados, rotaciones y patrones de animación.
Este anillo compacto de 12 LED es adecuado para indicadores, iluminación decorativa, robótica, dispositivos portátiles, relojes y pequeños proyectos de visualización.
