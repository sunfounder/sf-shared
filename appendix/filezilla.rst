.. note::

    ¡Hola! Bienvenido a la comunidad de entusiastas de SunFounder Raspberry Pi, Arduino y ESP32 en Facebook. Sumérgete en el mundo de Raspberry Pi, Arduino y ESP32 con otros entusiastas.

    **¿Por qué unirse?**

    - **Soporte experto**: Resuelve problemas post-venta y desafíos técnicos con la ayuda de nuestra comunidad y equipo.
    - **Aprender y compartir**: Intercambia consejos y tutoriales para mejorar tus habilidades.
    - **Avances exclusivos**: Obtén acceso anticipado a nuevos anuncios de productos y adelantos.
    - **Descuentos especiales**: Disfruta de descuentos exclusivos en nuestros productos más nuevos.
    - **Promociones y sorteos festivos**: Participa en sorteos y promociones festivas.

    👉 ¿Listo para explorar y crear con nosotros? Haz clic en [|link_sf_facebook|] y únete hoy mismo!

.. _filezilla:

Software FileZilla
====================

.. image:: /_shared/appendix/img/filezilla_icon.png
   :width: 20%

El Protocolo de Transferencia de Archivos (FTP) se utiliza comúnmente para transferir archivos entre computadoras a través de una red.  
**FileZilla** es un cliente de código abierto que admite FTP, FTPS y **SFTP** (recomendado para Raspberry Pi).  
Con FileZilla, puedes subir fácilmente archivos (como imágenes, audio y scripts) desde tu computadora a la Raspberry Pi, o descargar archivos desde la Pi a tu computadora.

Descargar FileZilla
------------------------

.. |shared_link_filezilla| raw:: html

    <a href="https://filezilla-project.org/" target="_blank">FileZilla</a> 

#. Visita el sitio web oficial de |shared_link_filezilla| y descarga **FileZilla Client** para tu sistema operativo.

#. Instala y ejecuta el programa.

   .. image:: /_shared/appendix/img/filezilla_install.png

#. Abre FileZilla e introduce la siguiente información:

   * **Host:** ``<hostname>.local`` o la dirección IP de la Raspberry Pi  
   * **Username:** tu nombre de usuario de la Pi  
   * **Password:** la contraseña configurada en Raspberry Pi Imager  
   * **Port:** ``22`` (para SFTP)
   * Haz clic en **Quickconnect** (o presiona **Enter**) para establecer la conexión.

   .. image:: /_shared/appendix/img/filezilla_connect.png
      :align: center

#. Una vez conectado, el panel izquierdo muestra tus **archivos locales**, y el panel derecho muestra los **archivos de la Raspberry Pi**.

    .. image:: /_shared/appendix/img/filezilla_in.png
       :align: center

#. Puedes:

   * **Subir** un archivo: arrástralo del panel izquierdo → panel derecho  
   * **Descargar** un archivo: arrástralo del panel derecho → panel izquierdo  

   FileZilla iniciará la transferencia inmediatamente y el estado se mostrará en el panel inferior.
