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

  La Raspberry Pi actúa como el **cerebro**, encargándose de todas las tareas de computación, sensores y control.  
  
  .. image:: /_shared/pi_start/img/need_pi.jpg

  * **Modelos compatibles**: Raspberry Pi 5, Raspberry Pi 4, 3 o Raspberry Pi Zero 2W  
  * **Mínimo**: **2GB de RAM** — suficiente para todos los proyectos estándar en Python y para usar **servicios de IA en línea** como OpenAI Whisper, TTS o LLMs.  
  * **Recomendado**: **4GB de RAM o más** — garantiza un rendimiento más fluido al ejecutar **modelos de IA locales** (por ejemplo, reconocimiento de voz Vosk, Piper TTS o LLMs ligeros) junto con transmisión de cámara y tareas de control.  
  

* **Adaptador de alimentación**

  Este kit incluye un **paquete de baterías 18650** y una placa **Fusion HAT+** con un circuito de carga integrado.
  
  .. image:: /_shared/pi_start/img/need_power.png
    :width: 400

  * Para la carga, se recomienda utilizar una **fuente de alimentación de 5V 3A**, como el **adaptador oficial Raspberry Pi USB-C de 15W**.  
  * También puedes usar un **cargador USB-C Power Delivery (PD)** o un **cargador rápido QC 2.0**.  
  * Una carga completa suele tardar aproximadamente **2 horas** (del 0% al 100%).  


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
 
  Los diferentes modelos de Raspberry Pi utilizan distintos conectores HDMI; asegúrate de comprobar tu modelo de Pi y preparar el cable correcto. 
  
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
* ¿No sabes qué comprar? La opción más estable y universal es: **Raspberry Pi 4 (2GB) + fuente de alimentación oficial + tarjeta Micro SD de 32GB**.  
