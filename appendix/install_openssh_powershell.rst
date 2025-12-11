.. note::

    ¡Hola, bienvenido a la comunidad de entusiastas de SunFounder Raspberry Pi & Arduino & ESP32 en Facebook! Sumérgete más en Raspberry Pi, Arduino y ESP32 con otros entusiastas.

    **¿Por qué unirse?**

    - **Soporte experto**: Resuelve problemas postventa y desafíos técnicos con la ayuda de nuestra comunidad y equipo.
    - **Aprender y compartir**: Intercambia consejos y tutoriales para mejorar tus habilidades.
    - **Previsualizaciones exclusivas**: Obtén acceso temprano a anuncios de nuevos productos y adelantos exclusivos.
    - **Descuentos especiales**: Disfruta de descuentos exclusivos en nuestros productos más nuevos.
    - **Promociones y sorteos festivos**: Participa en sorteos y promociones festivas.

    👉 ¿Listo para explorar y crear con nosotros? Haz clic en [|link_sf_facebook|] y únete hoy mismo.

.. _openssh_powershell:

Instalar OpenSSH mediante PowerShell
====================================

Si ves el siguiente error al ejecutar ``ssh <username>@<hostname>.local`` o ``ssh <username>@<IP>``:

.. code-block::

    ssh: The term 'ssh' is not recognized as the name of a cmdlet, function, script file, or operable program.

Significa que tu sistema Windows no tiene OpenSSH instalado.  
Sigue los pasos a continuación para instalarlo manualmente.

#. Abre el Menú Inicio de Windows, escribe **powershell**, haz clic derecho en **Windows PowerShell** y selecciona **Run as administrator** (Ejecutar como administrador).

   .. image:: /_shared/appendix/img/powershell_ssh.png
      :align: center

#. Instala el cliente OpenSSH:

   .. code-block:: bash

      Add-WindowsCapability -Online -Name OpenSSH.Client~~~~0.0.1.0

#. Tras la instalación, deberías ver una salida similar a:

   .. code-block::

        Path          :
        Online        : True
        RestartNeeded : False

#. Verifica la instalación:

   .. code-block:: bash

      Get-WindowsCapability -Online | Where-Object Name -like 'OpenSSH*'

#. Si OpenSSH está instalado, la salida incluirá:

   .. code-block::

        Name  : OpenSSH.Client~~~~0.0.1.0
        State : Installed
        Name  : OpenSSH.Server~~~~0.0.1.0
        State : NotPresent

   .. warning::
      Si ``Installed`` no aparece, es posible que tu sistema Windows sea demasiado antiguo.  
      En ese caso, recomendamos usar una herramienta SSH de terceros. Consulta: :ref:`login_windows`

#. Cierra PowerShell, vuelve a abrirlo (esta vez no es necesario usar administrador) y utiliza el comando ``ssh`` para iniciar sesión:

   .. code-block:: bash

      ssh <username>@<hostname>.local

   .. image:: /_shared/appendix/img/powershell_login.png
      :align: center


