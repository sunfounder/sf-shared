.. note::

    ¡Hola, bienvenido a la comunidad de entusiastas de SunFounder Raspberry Pi & Arduino & ESP32 en Facebook! Sumérgete más en Raspberry Pi, Arduino y ESP32 con otros entusiastas.

    **¿Por qué unirse?**

    - **Soporte experto**: Resuelve problemas postventa y desafíos técnicos con la ayuda de nuestra comunidad y equipo.
    - **Aprender y compartir**: Intercambia consejos y tutoriales para mejorar tus habilidades.
    - **Previsualizaciones exclusivas**: Obtén acceso temprano a anuncios de nuevos productos y adelantos exclusivos.
    - **Descuentos especiales**: Disfruta de descuentos exclusivos en nuestros productos más nuevos.
    - **Promociones y sorteos festivos**: Participa en sorteos y promociones festivas.

    👉 ¿Listo para explorar y crear con nosotros? Haz clic en [|link_sf_facebook|] y únete hoy mismo.

¿Qué Más Necesitas?
===============================

Antes de comenzar a usar este kit, preparemos el hardware esencial.

Componentes Requeridos
------------------------------

* **Raspberry Pi**

  La Raspberry Pi actúa como el **cerebro**, encargándose de todas las tareas de cómputo, sensado y control.  
  
  .. image:: /_shared/pi_start/img/need_pi.jpg

  * **Modelos compatibles**: Raspberry Pi 5, Raspberry Pi 4, 3 o Raspberry Pi Zero 2W  
  * **Mínimo**: **2GB RAM** — suficiente para proyectos estándar de Python y para usar **servicios de IA en línea** como OpenAI Whisper, TTS o LLMs.  
  * **Recomendado**: **4GB RAM o más** — garantiza un rendimiento más fluido al ejecutar **modelos de IA locales** (p. ej., reconocimiento de voz Vosk, TTS Piper o LLMs ligeros) junto con transmisión de cámara y tareas de control.  
  

* **Adaptador de Corriente**

  Este kit incluye un **paquete de baterías 18650** y una placa **Fusion HAT** con un circuito de carga integrado.
  
  .. image:: /_shared/pi_start/img/need_power.png
    :width: 400

  * Para cargar, se recomienda usar una **fuente de alimentación de 5V 3A**, como el **adaptador oficial Raspberry Pi de 15W USB-C**.  
  * También puedes usar un cargador **USB-C Power Delivery (PD)** o un cargador rápido **QC 2.0**.  
  * Una carga completa suele tardar alrededor de **2 horas** (de 0% a 100%).  


* **Tarjeta Micro SD**

  La Raspberry Pi no tiene un disco duro integrado. Se inicia y almacena todos los archivos en una **tarjeta Micro SD**.  
  
  .. image:: /_shared/pi_start/img/need_sd.jpg
    :width: 200

  * Mínimo: **16GB**  
  * Recomendado: **32GB** para mayor estabilidad  
  * Marca: Usa opciones confiables como **SanDisk** o **Samsung** para evitar errores de lectura/escritura  
  
Componentes Opcionales
------------------------

Aunque no son estrictamente necesarios, los siguientes periféricos mejorarán considerablemente tu experiencia de aprendizaje y depuración:

* **Monitor (HDMI o TV)** 

  Para principiantes, recomendamos encarecidamente usar una pantalla con entrada HDMI para configurar fácilmente Raspberry Pi OS y ejecutar programas gráficos.  

  .. image:: /_shared/pi_start/img/need_screen.png
    :width: 400

* **Cable HDMI (Estándar / Mini / Micro)**
 
  Diferentes modelos de Raspberry Pi usan diferentes conectores HDMI; asegúrate de preparar el cable correcto: 
  
  * **Raspberry Pi 4 / 5**: Micro HDMI  
  * **Raspberry Pi 3**: HDMI estándar  
  * **Raspberry Pi Zero 2W**: Mini HDMI 

  .. image:: /_shared/pi_start/img/need_hdmi.png
    :width: 400

* **Teclado y Ratón**

  Muy útiles durante la configuración inicial de Raspberry Pi OS. Más adelante podrás usar acceso remoto (SSH/VNC), pero para principiantes recomendamos preparar un conjunto USB o inalámbrico básico.  

  .. image:: /_shared/pi_start/img/need_keyboard_mouse.png
    :width: 500
 

**Consejos de Preparación**

* Si compraste este kit, la mayoría de los accesorios vienen incluidos, pero aún necesitas preparar la placa Raspberry Pi, la tarjeta Micro SD y el adaptador de corriente por separado.  
* ¿No sabes qué comprar? La opción más estable y universal es: **Raspberry Pi 4 (2GB) + Fuente de Alimentación Oficial + Tarjeta Micro SD de 32GB**.  
