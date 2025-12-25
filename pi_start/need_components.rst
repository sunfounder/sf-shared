.. note::

    ¡Hola, bienvenido a la comunidad de entusiastas de SunFounder Raspberry Pi & Arduino & ESP32 en Facebook! Sumérgete más en Raspberry Pi, Arduino y ESP32 con otros entusiastas.

    **¿Por qué unirse?**

    - **Soporte experto**: Resuelve problemas postventa y desafíos técnicos con la ayuda de nuestra comunidad y equipo.
    - **Aprender y compartir**: Intercambia consejos y tutoriales para mejorar tus habilidades.
    - **Previsualizaciones exclusivas**: Obtén acceso temprano a anuncios de nuevos productos y adelantos exclusivos.
    - **Descuentos especiales**: Disfruta de descuentos exclusivos en nuestros productos más nuevos.
    - **Promociones y sorteos festivos**: Participa en sorteos y promociones festivas.

    👉 ¿Listo para explorar y crear con nosotros? Haz clic en [|link_sf_facebook|] y únete hoy mismo.

¿Qué más necesitas?
===============================

Antes de empezar a jugar con este kit, preparemos el hardware esencial.

Componentes necesarios
------------------------------

* **Raspberry Pi**

  La Raspberry Pi actúa como el **cerebro**, gestionando todas las tareas de computación, sensores y control.  
  
  * **Modelos compatibles**: Raspberry Pi 5, Raspberry Pi 4, 3 o Raspberry Pi Zero 2W  

  .. image:: /_shared/pi_start/img/need_pi.jpg

  
* **Adaptador de alimentación**

  Prepara una fuente de alimentación adecuada según tu modelo de Raspberry Pi:

  .. image:: /_shared/pi_start/img/need_power.png
    :width: 400

  - **Raspberry Pi 5**: 5V 5A USB-C (recomendado: fuente de alimentación oficial PD de 27W).  
  - **Raspberry Pi 4**: 5V 3A USB-C.  
  - **Raspberry Pi 3B/3B+**: 5V 2,5A Micro-USB.  
  - **Raspberry Pi Zero 2W**: 5V 2A Micro-USB.

  Utilizar una fuente de alimentación estable ayuda a evitar problemas de bajo voltaje y garantiza un funcionamiento fiable.

* **Tarjeta Micro SD**

  La Raspberry Pi no tiene un disco duro integrado. Arranca y almacena todos los archivos en una **tarjeta Micro SD**.  
  
  .. image:: /_shared/pi_start/img/need_sd.jpg
    :width: 200

  * Mínimo: **16GB**  
  * Recomendado: **32GB** para una mejor estabilidad  
  * Marca: utiliza opciones fiables como **SanDisk** o **Samsung** para evitar errores de lectura/escritura  
  

Componentes opcionales
------------------------

Aunque no son estrictamente necesarios, los siguientes periféricos mejorarán enormemente tu experiencia de aprendizaje y depuración:

* **Monitor (HDMI o TV)** 

  Para principiantes, recomendamos encarecidamente una pantalla con entrada HDMI, para que puedas configurar fácilmente Raspberry Pi OS y ejecutar programas gráficos.  

  .. image:: /_shared/pi_start/img/need_screen.png
    :width: 400

* **Cable HDMI (Estándar / Mini / Micro)**
 
  Los distintos modelos de Raspberry Pi utilizan diferentes conectores HDMI; asegúrate de comprobar tu modelo de Pi y preparar el cable correcto. 
  
  * **Raspberry Pi 4 / 5**: Micro HDMI  
  * **Raspberry Pi 3**: HDMI estándar  
  * **Raspberry Pi Zero 2W**: Mini HDMI 

  .. image:: /_shared/pi_start/img/need_hdmi.png
    :width: 400

* **Teclado y ratón**

  Muy útiles durante la configuración inicial de Raspberry Pi OS. Más adelante, puedes cambiar al acceso remoto (SSH/VNC), pero para principiantes recomendamos preparar un conjunto básico USB o inalámbrico.  

  .. image:: /_shared/pi_start/img/need_keyboard_mouse.png
    :width: 500
 

**Consejos de preparación**

* Si compraste este kit, la mayoría de los accesorios están incluidos, pero aún necesitas preparar por separado la placa Raspberry Pi, la tarjeta Micro SD y el adaptador de alimentación.  
* ¿No sabes qué comprar? La opción más estable y universal es: **Raspberry Pi 4/5 (2GB) + fuente de alimentación oficial + tarjeta Micro SD de 32GB**.  
