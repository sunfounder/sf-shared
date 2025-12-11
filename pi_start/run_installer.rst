.. note::

    ¡Hola, bienvenido a la comunidad de entusiastas de SunFounder Raspberry Pi & Arduino & ESP32 en Facebook! Sumérgete más en Raspberry Pi, Arduino y ESP32 con otros entusiastas.

    **¿Por qué unirse?**

    - **Soporte experto**: Resuelve problemas postventa y desafíos técnicos con la ayuda de nuestra comunidad y equipo.
    - **Aprender y compartir**: Intercambia consejos y tutoriales para mejorar tus habilidades.
    - **Previsualizaciones exclusivas**: Obtén acceso temprano a anuncios de nuevos productos y adelantos exclusivos.
    - **Descuentos especiales**: Disfruta de descuentos exclusivos en nuestros productos más nuevos.
    - **Promociones y sorteos festivos**: Participa en sorteos y promociones festivas.

    👉 ¿Listo para explorar y crear con nosotros? Haz clic en [|link_sf_facebook|] y únete hoy mismo.


.. _install_all_modules:

Configurar la Alimentación e Instalar el Software (Importante)
================================================================

En este capítulo instalarás el software relacionado, configurarás el audio, establecerás una gestión segura de energía y aprenderás cómo manejar los apagados correctamente.

.. _install_fusion_hat:

Instalar el módulo ``fusion-hat``
----------------------------------

Para este kit, todas las funciones GPIO se gestionan a través del Fusion HAT. Por lo tanto, debes usar la biblioteca correspondiente ``fusion-hat`` para acceder y controlarlas.

Ejecuta el siguiente comando en la terminal para instalar el módulo ``fusion-hat``:

   .. raw:: html

      <run></run>

   .. code-block::

      curl -sSL https://raw.githubusercontent.com/sunfounder/sunfounder-installer-scripts/main/install-fusion-hat.sh | sudo bash

.. note:: Para más detalles sobre fusion-hat, consulta |shared_link_fusion_hat|.


Cuando finalice la instalación, reinicia la Raspberry Pi. Luego ejecuta el script de configuración de audio:

   .. raw:: html

      <run></run>

   .. code-block::

      sudo /opt/setup_fusion_hat_audio.sh

Esto completa el proceso de instalación del software para el Fusion HAT.

Configurar y Usar el Apagado Seguro
-----------------------------------

El Fusion HAT depende de la señal de apagado de la Raspberry Pi para gestionar completamente la alimentación del sistema.  
Para garantizar un proceso de apagado seguro y confiable, debes **configurar el comportamiento de apagado** según el modelo de tu Raspberry Pi y luego usar correctamente el **botón de encendido**.

**Para Raspberry Pi 5 y 4B**

Estos modelos admiten un apagado completo. El Fusion HAT monitorea la línea de 3.3V para detectar el estado de energía de la Pi.

1. Coloca el jumper en **RPI_STATE → Pi3V3**.

   .. image:: /_shared/pi_start/img/state_3v3.jpg
      :width: 400

2. Edita la configuración del EEPROM manualmente:

   .. code-block::

      sudo raspi-config

3. Navega a **Advanced Options → A12 Shutdown Behaviour**.

   .. image:: /_shared/pi_start/img/shutdown_behaviour.png

4. Selecciona **B1 Full Power Off**.

   .. image:: /_shared/pi_start/img/run_power_off.png

5. Guarda los cambios. Se te pedirá reiniciar para que la nueva configuración surta efecto.

**Para Raspberry Pi Zero 2W, 3B, 3B+**

Estos modelos **no** admiten apagado completo usando 3.3V. En su lugar, se debe configurar el GPIO26 como indicador de estado de apagado.

1. Coloca el jumper en **RPI_STATE → IO26**.

   .. image:: /_shared/pi_start/img/state_io26.jpg
      :width: 400

2. Edita el archivo ``/boot/firmware/config.txt``:

   .. code-block::

      sudo nano /boot/firmware/config.txt

3. Agrega la siguiente línea al final para establecer el GPIO26 como bajo en apagado y alto al encender:

   .. code-block::

      dtoverlay=gpio-poweroff,gpio_pin=26,active_low=1

4. Reinicia para aplicar los cambios:

   .. code-block::

      sudo reboot

**Uso del Botón de Encendido para Apagado Seguro**

Una vez completada la configuración de apagado, puedes apagar el PiCar-X de forma segura usando el botón de encendido del Fusion HAT.

* **Apagado Suave (Recomendado)**

  * Mantén presionado el botón de encendido durante **2 segundos**.  
  * Los dos LED de alimentación parpadearán rápidamente.  
  * Suelta el botón → Fusion HAT iniciará el apagado de la Raspberry Pi.  
  * Una vez que finalice el apagado, Fusion HAT cortará la alimentación automáticamente.  
  * Esto protege tu tarjeta SD y tus archivos.

* **Apagado Forzado (Solo Emergencias)**

  * Si el sistema no responde, mantén presionado el botón durante **más de 5 segundos**.  
  * Fusion HAT forzará el apagado inmediato.  
  * Advertencia: Esto puede dañar la tarjeta SD o corromper archivos del sistema. Úsalo solo cuando sea estrictamente necesario.
