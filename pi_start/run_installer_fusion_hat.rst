.. note::

    ¡Hola, bienvenido a la comunidad de entusiastas de SunFounder Raspberry Pi & Arduino & ESP32 en Facebook! Sumérgete más en Raspberry Pi, Arduino y ESP32 con otros entusiastas.

    **¿Por qué unirse?**

    - **Soporte experto**: Resuelve problemas postventa y desafíos técnicos con la ayuda de nuestra comunidad y equipo.
    - **Aprender y compartir**: Intercambia consejos y tutoriales para mejorar tus habilidades.
    - **Previsualizaciones exclusivas**: Obtén acceso temprano a anuncios de nuevos productos y adelantos exclusivos.
    - **Descuentos especiales**: Disfruta de descuentos exclusivos en nuestros productos más nuevos.
    - **Promociones y sorteos festivos**: Participa en sorteos y promociones festivas.

    👉 ¿Listo para explorar y crear con nosotros? Haz clic en [|link_sf_facebook|] y únete hoy mismo.


.. _install_all_modules_fusion_hat:

Configurar Energía e Instalar Software (Importante)
================================================================

En este capítulo, instalarás el software relacionado, configurarás el audio, establecerás una gestión segura de la energía y aprenderás cómo manejar los apagados.

.. start_install_fusion_hat



Instalar el módulo ``fusion-hat``
------------------------------------

Para este kit, todas las funcionalidades GPIO se gestionan a través del Fusion HAT+. Por lo tanto, necesitas usar la biblioteca ``fusion-hat`` que lo acompaña para acceder y controlar dichas funciones.

Ejecuta el siguiente comando en la terminal para instalar el módulo ``fusion-hat``.

   .. raw:: html

      <run></run>

   .. code-block::

      curl -sSL https://raw.githubusercontent.com/sunfounder/sunfounder-installer-scripts/main/install-fusion-hat.sh | sudo bash

.. |shared_link_fusion_hat| raw:: html

    <a href="https://docs.sunfounder.com/projects/fusion-hat/en/latest/" target="_blank">Fusion HAT+</a>

.. note:: Para más detalles sobre fusion-hat, consulta |shared_link_fusion_hat|.


Después de que la instalación finalice, reinicia la Raspberry Pi. Luego ejecuta el script de configuración de audio:

   .. raw:: html

      <run></run>

   .. code-block::

      sudo /opt/setup_fusion_hat_audio.sh

Esto completa el proceso de instalación del software para el Fusion HAT+.

.. end_install_fusion_hat

.. start_configure_safe_shutdown

Configurar y Usar Apagado Seguro
-----------------------------------

El Fusion HAT+ depende de la señal de apagado de la Raspberry Pi para gestionar completamente la alimentación del sistema.  
Para garantizar un proceso de apagado seguro y confiable, debes **configurar el comportamiento de apagado** según el modelo de tu Raspberry Pi y luego usar correctamente el **botón de encendido**.

**Para Raspberry Pi 5 y 4B**

Estos modelos admiten el apagado completo después del cierre del sistema. El Fusion HAT+ supervisa la línea de 3.3V para detectar el estado de energía de la Raspberry Pi.

1. Coloca el jumper en **RPI_STATE → Pi3V3**.

   .. image:: /_shared/pi_start/img/state_3v3.jpg
      :width: 400

2. Edita manualmente la configuración del EEPROM:

   .. code-block::

      sudo raspi-config

3. Navega a **Advanced Options → A12 Shutdown Behaviour**.

   .. image:: /_shared/pi_start/img/shutdown_behaviour.png

4. Selecciona **B1 Full Power Off**.

   .. image:: /_shared/pi_start/img/run_power_off.png

5. Guarda los cambios. Se te pedirá reiniciar para que la nueva configuración entre en vigor.

**Para Raspberry Pi Zero 2W, 3B, 3B+**

Estos modelos **no** admiten el apagado completo usando 3.3V. En su lugar, el GPIO26 debe configurarse como indicador del estado de apagado.

1. Coloca el jumper en **RPI_STATE → IO26**.

   .. image:: /_shared/pi_start/img/state_io26.jpg
      :width: 400

2. Edita el archivo ``/boot/firmware/config.txt``:

   .. code-block::

      sudo nano /boot/firmware/config.txt

3. Agrega la siguiente línea al final para configurar el GPIO26 en bajo durante el apagado y en alto al encender:

   .. code-block::

      dtoverlay=gpio-poweroff,gpio_pin=26,active_low=1

4. Reinicia para aplicar los cambios:

   .. code-block::

      sudo reboot

**Uso del Botón de Encendido para un Apagado Seguro**

Después de completar la configuración de apagado, puedes apagar de forma segura el PiCar-X usando el botón de encendido del Fusion HAT+.

* **Apagado Suave (Recomendado)**

  * Mantén presionado el botón de encendido durante **2 segundos**.  
  * Los dos LED de alimentación parpadearán rápidamente.  
  * Suelta el botón → el Fusion HAT+ inicia el apagado de la Raspberry Pi.  
  * Una vez que el apagado se completa, el Fusion HAT+ cortará la alimentación automáticamente.  
  * Esto protege tu tarjeta SD y los archivos.

* **Apagado Forzado (Solo Emergencias)**

  * Si el sistema no responde, mantén presionado el botón de encendido durante **5 segundos o más**.  
  * El Fusion HAT+ forzará el corte de energía.  
  * Advertencia: esto puede dañar la tarjeta SD o los archivos del sistema. Úsalo solo cuando sea absolutamente necesario.

.. end_configure_safe_shutdown
