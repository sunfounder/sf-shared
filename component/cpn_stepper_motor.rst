Stepper Motor and ULN2003 Module
=========================================

**Motor Paso a Paso**

El 28BYJ-48 es un motor paso a paso unipolar de 5 hilos que funciona a 5 V. Los motores paso a paso son motores de precisión que pueden controlarse con gran exactitud sin necesidad de retroalimentación de sensores. Esto se debe a que el eje del motor está equipado con imanes y es controlado por bobinas electromagnéticas que se encienden y apagan en una secuencia específica, haciendo que el eje se mueva en pequeños pasos precisos.

.. image:: img/step_stepper.png
  :align: center

El estator del motor paso a paso que utilizamos tiene 32 polos magnéticos, por lo que una vuelta completa requiere 32 pasos. El eje de salida del motor paso a paso está conectado a un conjunto de engranajes reductores, y la relación de reducción es de 1/64. Por lo tanto, el eje de salida final gira una vuelta completa requiriendo 32*64 = 2048 pasos.

**Cómo Funciona un Motor Paso a Paso Unipolar**

Un motor paso a paso unipolar normalmente tiene cuatro fases y funciona con corriente continua. Al temporizar correctamente la corriente eléctrica aplicada a las fases del motor, puedes hacer que el motor gire paso a paso. Imagina que el centro del motor contiene un imán con forma de engranaje (el rotor) rodeado por varios dientes numerados del 0 al 5. Alrededor de estos dientes hay ocho polos magnéticos dispuestos en pares (A a D), conectados mediante bobinas.

.. image:: img/step_interal.png
  :align: center

Cuando activas diferentes interruptores conectados a estas bobinas (etiquetados como SA, SB, SC y SD), controlas qué polos magnéticos se activan. Por ejemplo, si el interruptor SB está encendido (y los demás están apagados), los polos magnéticos B se alinean con ciertos dientes del rotor, provocando su movimiento. Cuando luego activas el interruptor SC, el rotor gira para alinearse con los polos magnéticos C, y así sucesivamente. Al alternar cíclicamente los interruptores A, B, C y D, el rotor gira de forma continua.

**Módulo ULN2003**

.. image:: img/step_uln2003.png
    :align: center

El módulo controlador de motor paso a paso ULN2003 es fundamental para integrar el motor paso a paso en los circuitos. Funciona como un inversor de 7 canales, lo que significa que convierte las señales de entrada en las acciones de salida necesarias para el motor. Por ejemplo, si se envía una señal alta a IN1 y señales bajas a IN2, IN3 e IN4, entonces OUT1 se vuelve baja y las demás salidas permanecen altas, haciendo que el motor gire un paso. Al proporcionar secuencias específicas como esta, el motor puede girar de manera suave paso a paso. El ULN2003 simplifica el control de las secuencias de temporización necesarias para el funcionamiento del motor.
