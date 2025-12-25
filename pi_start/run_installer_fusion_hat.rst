.. note::

    Bonjour, bienvenue dans la communauté des passionnés de Raspberry Pi, Arduino et ESP32 de SunFounder sur Facebook ! Plongez dans l'univers de Raspberry Pi, Arduino et ESP32 avec d'autres passionnés.

    **Pourquoi nous rejoindre ?**

    - **Support d'experts** : Résolvez les problèmes après-vente et les défis techniques avec l'aide de notre communauté et de notre équipe.
    - **Apprendre et partager** : Échangez des conseils et des tutoriels pour améliorer vos compétences.
    - **Aperçus exclusifs** : Accédez en avant-première aux annonces de nouveaux produits et à des aperçus exclusifs.
    - **Réductions spéciales** : Profitez de réductions exclusives sur nos nouveaux produits.
    - **Promotions et cadeaux festifs** : Participez à des concours et à des promotions festives.

    👉 Prêt à explorer et à créer avec nous ? Cliquez sur [|link_sf_facebook|] et rejoignez-nous dès aujourd'hui !


.. _install_all_modules_fusion_hat:

Configurer l’alimentation et installer les logiciels (Important)
================================================================

Dans ce chapitre, vous allez installer les logiciels associés, configurer l’audio, mettre en place une gestion sécurisée de l’alimentation et apprendre à effectuer correctement l’arrêt du système.

.. start_install_fusion_hat

.. _install_fusion_hat:

Installer le module ``fusion-hat``
----------------------------------

Pour ce kit, toutes les fonctionnalités GPIO sont gérées via le Fusion HAT+. Vous devez donc utiliser la bibliothèque associée ``fusion-hat`` pour y accéder et les contrôler.

Exécutez la commande suivante dans le terminal pour installer le module ``fusion-hat``.

   .. raw:: html

      <run></run>

   .. code-block::

      curl -sSL https://raw.githubusercontent.com/sunfounder/sunfounder-installer-scripts/main/install-fusion-hat.sh | sudo bash

.. |shared_link_fusion_hat| raw:: html

    <a href="https://docs.sunfounder.com/projects/fusion-hat/en/latest/" target="_blank">Fusion HAT+</a>

.. note:: Pour plus de détails sur fusion-hat, veuillez consulter le |shared_link_fusion_hat|.


Une fois l’installation terminée, redémarrez le Raspberry Pi. Exécutez ensuite le script de configuration audio :

   .. raw:: html

      <run></run>

   .. code-block::

      sudo /opt/setup_fusion_hat_audio.sh

Cela termine le processus d’installation logicielle du Fusion HAT+.

Configurer et utiliser l’arrêt sécurisé
---------------------------------------

Le Fusion HAT+ s’appuie sur le signal d’arrêt du Raspberry Pi pour gérer complètement l’alimentation du système.  
Afin de garantir un processus d’extinction sûr et fiable, vous devez **configurer le comportement d’arrêt** en fonction de votre modèle de Raspberry Pi, puis utiliser correctement le **bouton d’alimentation**.

**Pour Raspberry Pi 5 et 4B**

Ces modèles prennent en charge une coupure complète de l’alimentation après l’arrêt. Le Fusion HAT+ surveille la ligne 3,3 V pour détecter l’état d’alimentation du Pi.

1. Placez le cavalier sur **RPI_STATE → Pi3V3**.

   .. image:: /_shared/pi_start/img/state_3v3.jpg
      :width: 400

2. Modifiez manuellement la configuration de l’EEPROM :

   .. code-block::

      sudo raspi-config

3. Accédez à **Advanced Options → A12 Shutdown Behaviour**.

   .. image:: /_shared/pi_start/img/shutdown_behaviour.png

4. Sélectionnez **B1 Full Power Off**.

   .. image:: /_shared/pi_start/img/run_power_off.png

5. Enregistrez les modifications. Il vous sera demandé de redémarrer afin que les nouveaux paramètres prennent effet.

**Pour Raspberry Pi Zero 2W, 3B, 3B+**

Ces modèles ne prennent **pas** en charge une coupure complète de l’alimentation via le 3,3 V. À la place, le GPIO26 doit être configuré comme indicateur d’état d’arrêt.

1. Placez le cavalier sur **RPI_STATE → IO26**.

   .. image:: /_shared/pi_start/img/state_io26.jpg
      :width: 400

2. Modifiez le fichier ``/boot/firmware/config.txt`` :

   .. code-block::

      sudo nano /boot/firmware/config.txt

3. Ajoutez la ligne suivante à la fin du fichier afin de définir GPIO26 à l’état bas lors de l’arrêt et à l’état haut au démarrage :

   .. code-block::

      dtoverlay=gpio-poweroff,gpio_pin=26,active_low=1

4. Redémarrez pour appliquer les modifications :

   .. code-block::

      sudo reboot

**Utilisation du bouton d’alimentation pour un arrêt sécurisé**

Une fois la configuration de l’arrêt terminée, vous pouvez éteindre le PiCar-X en toute sécurité à l’aide du bouton d’alimentation du Fusion HAT+.

* **Arrêt logiciel (recommandé)**

  * Appuyez et maintenez le bouton d’alimentation pendant **2 secondes**.  
  * Les deux voyants d’alimentation clignotent rapidement.  
  * Relâchez le bouton → le Fusion HAT+ déclenche l’arrêt du Raspberry Pi.  
  * Une fois l’arrêt terminé, le Fusion HAT+ coupe automatiquement l’alimentation.  
  * Cela protège la carte SD et les fichiers.

* **Arrêt forcé (urgence uniquement)**

  * Si le système ne répond plus, appuyez et maintenez le bouton d’alimentation pendant **plus de 5 secondes**.  
  * Le Fusion HAT+ forcera la coupure de l’alimentation.  
  * Avertissement : cela peut corrompre la carte SD ou les fichiers système. À utiliser uniquement en cas de nécessité.

.. end_install_fusion_hat
