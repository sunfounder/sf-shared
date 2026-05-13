.. note::

    Bonjour, bienvenue dans la communauté des passionnés de Raspberry Pi, Arduino et ESP32 de SunFounder sur Facebook ! Plongez dans l'univers de Raspberry Pi, Arduino et ESP32 avec d'autres passionnés.

    **Pourquoi nous rejoindre ?**

    - **Support d'experts** : Résolvez les problèmes après-vente et les défis techniques avec l'aide de notre communauté et de notre équipe.
    - **Apprendre et partager** : Échangez des conseils et des tutoriels pour améliorer vos compétences.
    - **Aperçus exclusifs** : Accédez en avant-première aux annonces de nouveaux produits et à des aperçus exclusifs.
    - **Réductions spéciales** : Profitez de réductions exclusives sur nos nouveaux produits.
    - **Promotions et cadeaux festifs** : Participez à des concours et à des promotions festives.

    👉 Prêt à explorer et à créer avec nous ? Cliquez sur [|link_sf_facebook|] et rejoignez-nous dès aujourd'hui !

.. _install_os:

Installation du système d'exploitation
======================================

.. start_imager

Avant d'utiliser votre Raspberry Pi, vous devez installer **Raspberry Pi OS** sur une carte microSD.
Ce guide explique comment procéder à l'aide de **Raspberry Pi Imager**, de manière simple et adaptée aux débutants.

**Composants requis**

* Un ordinateur (Windows, macOS ou Linux)
* Une carte microSD (16 Go ou plus ; marques recommandées : SanDisk, Samsung)
* Un lecteur de carte microSD

-------------------

Installer Raspberry Pi Imager
-------------------------------------------

.. |shared_link_rpi_imager| raw:: html

    <a href="https://www.raspberrypi.com/software/" target="_blank">Raspberry Pi Imager</a>

#. Visitez la page officielle de téléchargement de Raspberry Pi Imager : |shared_link_rpi_imager|. Téléchargez l'installateur correspondant à votre système d'exploitation.

   .. image:: /_shared/pi_start/img/imager_download.png
      :width: 70%

#. Suivez les étapes d'installation (langue, chemin d'installation, confirmation). Une fois l'installation terminée, lancez **Raspberry Pi Imager** depuis votre bureau ou le menu des applications.

   .. image:: /_shared/pi_start/img/imager_install.png
      :width: 90%

--------------------------------------

.. end_imager


.. start_install_os

Installer le système d'exploitation sur la carte microSD
------------------------------------------------

1. Insérez votre carte microSD dans votre ordinateur à l'aide d'un lecteur de carte. Sauvegardez toutes les données importantes avant de continuer.

   .. image:: /_shared/pi_start/img/insert_sd.png
      :width: 90%

2. Lorsque Raspberry Pi Imager s'ouvre, vous verrez la page **Device**. Sélectionnez votre modèle de Raspberry Pi dans la liste (par exemple Raspberry Pi 5, 4, 3 ou Zero 2W).

   .. image:: /_shared/pi_start/img/imager_device.png
      :width: 90%

.. end_install_os

3. Allez dans la section **OS** et choisissez l'option recommandée **Raspberry Pi OS (64-bit)**.

   .. image:: /_shared/pi_start/img/imager_os.png
      :width: 90%


.. start_storage

4. Dans la section **Storage**, sélectionnez votre carte microSD.

   .. image:: /_shared/pi_start/img/imager_storage.png
      :width: 90%

.. end_storage

-------------------

.. start_cutomization_os

.. _imager_custom:

Paramètres de personnalisation du système d'exploitation
------------------------------------------

#. Passez à l'étape de personnalisation.

   * Si vous connectez un moniteur, un clavier et une souris directement à votre Raspberry Pi, vous pouvez cliquer sur **SKIP CUSTOMISATION**.
   * Si vous prévoyez de configurer le Raspberry Pi en mode *headless* (accès distant via Wi-Fi), vous devez compléter les paramètres de personnalisation.

   .. image:: /_shared/pi_start/img/imager_custom_skip.png
      :width: 90%

#. **Définir le nom d'hôte**

   * Donnez un nom d'hôte unique à votre Raspberry Pi.
   * Vous pourrez vous y connecter ultérieurement via ``hostname.local``.

   .. image:: /_shared/pi_start/img/imager_custom_hostname.png
      :width: 90%

#. **Définir la localisation**

   * Choisissez votre capitale.
   * Imager complétera automatiquement le fuseau horaire et la disposition du clavier en fonction de votre sélection, mais vous pouvez les ajuster si nécessaire. Sélectionnez Next.

   .. image:: /_shared/pi_start/img/imager_custom_local.png
      :width: 90%

#. **Définir le nom d'utilisateur et le mot de passe**

   Créez un compte utilisateur pour votre Raspberry Pi.

   .. image:: /_shared/pi_start/img/imager_custom_user.png
      :width: 90%

#. **Configurer le Wi-Fi**

   * Saisissez le **SSID** (nom du réseau) et le **mot de passe** de votre Wi-Fi.
   * Votre Raspberry Pi se connectera automatiquement lors du premier démarrage.

   .. image:: /_shared/pi_start/img/imager_custom_wifi.png
      :width: 90%

#. **Activer SSH (optionnel mais recommandé)**

   * L'activation de SSH vous permet de vous connecter à distance depuis votre ordinateur.
   * Vous pouvez vous connecter à l'aide de votre nom d'utilisateur/mot de passe ou configurer des clés SSH.

   .. image:: /_shared/pi_start/img/imager_custom_ssh.png
      :width: 90%

.. end_cutomization_os

.. start_enable_connection

#. **Activer Raspberry Pi Connect (optionnel)**

   Raspberry Pi Connect vous permet d'accéder au bureau de votre Raspberry Pi depuis un navigateur web.

   * Activez **Raspberry Pi Connect**, puis cliquez sur **OPEN RASPBERRY PI CONNECT**.

     .. image:: /_shared/pi_start/img/imager_custom_connect.png
        :width: 90%

   * Le site web Raspberry Pi Connect s'ouvrira dans votre navigateur par défaut. Connectez-vous à votre compte Raspberry Pi ID ou inscrivez-vous si vous n'en avez pas encore.

     .. image:: /_shared/pi_start/img/imager_custom_open.png
        :width: 90%

   * Sur la page **New auth key**, créez votre clé d'authentification à usage unique.

      * Si votre compte Raspberry Pi ID ne fait partie d'aucune organisation, sélectionnez **Create auth key and launch Raspberry Pi Imager**.
      * Si vous appartenez à une ou plusieurs organisations, choisissez-en une, puis créez la clé et lancez Imager.
      * Assurez-vous d'allumer votre Raspberry Pi et de le connecter à Internet avant l'expiration de la clé.

     .. image:: /_shared/pi_start/img/imager_custom_authkey.png
        :width: 90%

   * Votre navigateur peut vous demander d'ouvrir Raspberry Pi Imager — autorisez-le.

     * Imager s'ouvrira sur l'onglet Raspberry Pi Connect et affichera le jeton d'authentification.
     * Si le jeton ne se transfère pas automatiquement, ouvrez la section **Having trouble?** sur la page Raspberry Pi Connect, copiez le jeton et collez-le manuellement dans Imager.

     .. image:: /_shared/pi_start/img/imager_custom_connect_token.png
        :width: 90%

.. end_enable_connection

-------------------

.. start_write_os

Écrire l'image du système d'exploitation
-----------------------------


#. Vérifiez tous les paramètres, puis cliquez sur **WRITE**.

   .. image:: /_shared/pi_start/img/imager_writing.png
      :width: 90%

#. Si la carte contient déjà des données, Raspberry Pi Imager affichera un avertissement indiquant que toutes les données du périphérique seront effacées. Vérifiez soigneusement que vous avez sélectionné le bon disque, puis cliquez sur **I UNDERSTAND, ERASE AND WRITE** pour continuer.

   .. image:: /_shared/pi_start/img/imager_erase.png
      :width: 90%

#. Attendez la fin de l'écriture et de la vérification. Une fois terminé, Raspberry Pi Imager affichera **Write complete!** ainsi qu'un récapitulatif de vos choix. Le périphérique de stockage sera automatiquement éjecté afin que vous puissiez le retirer en toute sécurité.


   .. image:: /_shared/pi_start/img/imager_finish.png
        :width: 90%

#. Retirez la carte microSD et insérez-la dans le logement situé sous votre Raspberry Pi. Votre Raspberry Pi est maintenant prêt à démarrer avec le nouveau système d'exploitation !

   .. image:: /_shared/pi_start/img/os_sd_to_pi.jpg
        :width: 70%

.. end_write_os
