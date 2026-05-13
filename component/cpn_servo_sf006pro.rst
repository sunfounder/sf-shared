.. note::

    ¡Hola, bienvenido a la comunidad de entusiastas de SunFounder Raspberry Pi & Arduino & ESP32 en Facebook! Sumérgete más en Raspberry Pi, Arduino y ESP32 con otros entusiastas.

    **¿Por qué unirse?**

    - **Soporte experto**: Resuelve problemas postventa y desafíos técnicos con la ayuda de nuestra comunidad y equipo.
    - **Aprender y compartir**: Intercambia consejos y tutoriales para mejorar tus habilidades.
    - **Previsualizaciones exclusivas**: Obtén acceso temprano a anuncios de nuevos productos y adelantos exclusivos.
    - **Descuentos especiales**: Disfruta de descuentos exclusivos en nuestros productos más nuevos.
    - **Promociones y sorteos festivos**: Participa en sorteos y promociones festivas.

    👉 ¿Listo para explorar y crear con nosotros? Haz clic en [|link_sf_facebook|] y únete hoy mismo.

.. _cpn_sf006pro_servo:

Servo SF006PRO
===================

.. image:: img/servo_metal.png
    :width: 50%
    :align: center

Este servo es un actuador pequeño y fiable que funciona con 4–6 V, ofreciendo un movimiento suave y hasta 180° de control. Proporciona un buen par, respuesta rápida y bajo consumo de energía, lo que lo hace adecuado para robótica, mecanismos y proyectos de hobby en general.
Su interfaz PWM estándar de 3 pines facilita la conexión a microcontroladores como Arduino o Raspberry Pi.

**Cómo funciona un servo**


Un servo típico consta de varios componentes internos:

* Carcasa
* Eje de salida
* Sistema de engranajes
* Potenciómetro
* Motor DC
* Placa de control (integrada)

El microcontrolador envía señales de control PWM al servo a través del pin de señal.
La placa de control interpreta la señal y acciona el motor DC, que hace girar el sistema de engranajes. Tras pasar por el sistema de reducción de engranajes, el eje gira con un par mayor.

El eje de salida está conectado mecánicamente al potenciómetro. A medida que el eje gira, el potenciómetro cambia su tensión de salida. La placa de control lee esta retroalimentación para determinar la posición actual, ajustando la rotación del motor hasta que el eje alcance y mantenga el ángulo objetivo.

.. image:: img/servo_internal.png
    :align: center

**Control PWM**

El ángulo de rotación del servo está determinado por la anchura del pulso PWM. El servo normalmente espera un pulso cada **20 ms**.

Comportamiento típico del pulso:

* **1,5 ms** → Posición neutra (aproximadamente 90°)
* **< 1,5 ms** → Se mueve en sentido antihorario desde el centro
* **> 1,5 ms** → Se mueve en sentido horario desde el centro

La mayoría de los servos de hobby aceptan anchos de pulso entre **0,5 ms y 2,5 ms**, correspondientes a su rango de movimiento completo.

.. image:: img/servo_duty.png
    :width: 600
    :align: center


**Parámetros**

.. list-table::
   :header-rows: 1
   :widths: 25 75

   * - Parámetro
     - Especificación

   * - Voltaje de funcionamiento
     - DC 4 V–6 V (Nominal 5 V, se recomienda usar fuente de 5 V)

   * - Corriente en espera
     - ≤ 5 mA

   * - Corriente sin carga
     - ≤ 350 mA a 5 V (pico medido manualmente)

   * - Corriente de bloqueo
     - ≤ 1,2 A a 5 V (cae a ≤ 250 mA tras 5 segundos de bloqueo)

   * - Par nominal
     - 0,75 kgf·cm (a 5 V)

   * - Carga dinámica máxima
     - ≥ 2,2 kgf·cm (a 5 V)

   * - Par de bloqueo (estático)
     - ≥ 5 kgf·cm (probado con medidor de par)

   * - Velocidad sin carga
     - ≤ 0,17 seg/60° (a 5 V)

   * - Ángulo de recorrido operativo
     - 90° ±10° (1000–2000 μs)

   * - Ángulo máximo de funcionamiento
     - 180° ±10° (500–2500 μs)

   * - Ángulo límite mecánico
     - 360°

   * - Rango de anchura de pulso
     - 500 μs ~ 2500 μs

   * - Posición neutra
     - 1500 μs

   * - Ancho de banda muerta
     - ≤ 6 μs

   * - Juego mecánico
     - ≤ 0,5°

   * - Peso
     - 13,5 ± 0,5 g

   * - Material de engranajes
     - Engranajes híbridos de plástico + metal

   * - Tipo de motor
     - Motor de núcleo de hierro

   * - Tipo de potenciómetro
     - Película de carbono, ángulo 220°, ≥ 100.000 ciclos

   * - Cable
     - 250 ±5 mm, conector JR de 3 pines (Marrón–Rojo–Naranja)

   * - Pines del conector
     - Naranja: Señal PWM

       Rojo: VCC

       Marrón: GND

   * - Interfaz de comunicación
     - PWM

       Voltaje de señal: ALTO 2,0–5,0 V / BAJO 0,0–0,6 V

       Frecuencia de trama: 3–30 ms (Predeterminado 20 ms)

       Rango de pulso: 500–2500 μs

**Dimensiones**

.. image:: img/servo_metal_size.png
    :width: 80%
    :align: center
