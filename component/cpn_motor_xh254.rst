.. note::

    ¡Hola, bienvenido a la comunidad de entusiastas de SunFounder Raspberry Pi & Arduino & ESP32 en Facebook! Sumérgete más en Raspberry Pi, Arduino y ESP32 con otros entusiastas.

    **¿Por qué unirse?**

    - **Soporte experto**: Resuelve problemas postventa y desafíos técnicos con la ayuda de nuestra comunidad y equipo.
    - **Aprender y compartir**: Intercambia consejos y tutoriales para mejorar tus habilidades.
    - **Previsualizaciones exclusivas**: Obtén acceso temprano a anuncios de nuevos productos y adelantos exclusivos.
    - **Descuentos especiales**: Disfruta de descuentos exclusivos en nuestros productos más nuevos.
    - **Promociones y sorteos festivos**: Participa en sorteos y promociones festivas.

    👉 ¿Listo para explorar y crear con nosotros? Haz clic en [|link_sf_facebook|] y únete hoy mismo.

.. _cpn_motor_xh254:

Motor DC XH2.54
===================

.. image:: img/motor_254_pic.png
    :width: 50%
    :align: center

Un motor de corriente continua (DC) es un actuador eléctrico simple que convierte la energía eléctrica en rotación mecánica.
Se utiliza ampliamente en dispositivos como bombas, ventiladores, compresores y pequeños robots gracias a su capacidad para proporcionar movimiento rotativo continuo.

**Especificaciones del motor**

* **Voltaje de funcionamiento**: 3–5 V
* **Corriente en vacío (3 V)**: 100–120 mA
* **Velocidad en vacío (3 V)**: 8000 RPM
* **Par de arranque (3 V)**: 140 g·cm
* **Corriente de bloqueo (3 V)**: 650 mA
* **Tipo de conector**: XH2.54 2P (blanco)
* **Longitud del cable**: Rojo/Negro, 10 cm, 24 AWG
* **Dimensiones**: 25 × 20 × 15 mm

Un motor DC consta de dos componentes principales: el **estator**, que permanece fijo, y el **rotor** (o **inducido**), que gira para generar movimiento.
El rotor se coloca dentro de un campo magnético creado por imanes permanentes. Cuando la corriente fluye a través de los devanados del inducido, produce un campo magnético que interactúa con el campo del estator, generando un par que provoca la rotación.

.. image:: img/motor_sche.png
    :align: center

La corriente fluye desde la fuente de alimentación a las escobillas, al conmutador y luego a los devanados del inducido.
El conmutador invierte periódicamente la dirección de la corriente cada media vuelta, asegurando que el par actúe siempre en la dirección correcta para mantener una rotación continua.
Esta acción de conmutación convierte efectivamente la alimentación DC en una forma de corriente alterna dentro del motor, permitiendo un movimiento suave y sostenido.
