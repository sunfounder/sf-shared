.. note::

    Bonjour, bienvenue dans la communauté des passionnés de Raspberry Pi, Arduino et ESP32 de SunFounder sur Facebook ! Plongez dans l'univers de Raspberry Pi, Arduino et ESP32 avec d'autres passionnés.

    **Pourquoi nous rejoindre ?**

    - **Support d'experts** : Résolvez des problèmes après-vente et des défis techniques grâce à l'aide de notre communauté et de notre équipe.
    - **Apprendre et partager** : Échangez des astuces et des tutoriels pour améliorer vos compétences.
    - **Aperçus exclusifs** : Obtenez un accès anticipé aux annonces de nouveaux produits et aux avant-premières.
    - **Réductions exclusives** : Profitez de réductions spéciales sur nos derniers produits.
    - **Promotions et cadeaux festifs** : Participez à des concours et promotions festifs.

    👉 Prêt à explorer et à créer avec nous ? Cliquez sur [|link_sf_facebook|] et rejoignez-nous dès aujourd'hui !

.. _filezilla:

Logiciel FileZilla
====================

.. image:: /_shared/appendix/img/filezilla_icon.png
   :width: 20%

Le protocole de transfert de fichiers (FTP) est couramment utilisé pour transférer des fichiers entre des ordinateurs via un réseau.  
**FileZilla** est un client open source qui prend en charge FTP, FTPS et **SFTP** (recommandé pour Raspberry Pi).  
Avec FileZilla, vous pouvez facilement téléverser des fichiers (tels que des images, de l’audio et des scripts) depuis votre ordinateur vers le Raspberry Pi, ou télécharger des fichiers du Pi vers votre ordinateur.

Télécharger FileZilla
-----------------------

.. |shared_link_filezilla| raw:: html

    <a href="https://filezilla-project.org/" target="_blank">FileZilla</a> 

#. Visitez le site officiel |shared_link_filezilla| et téléchargez **FileZilla Client** pour votre système d’exploitation.

#. Installez et lancez le programme.

   .. image:: /_shared/appendix/img/filezilla_install.png

#. Ouvrez FileZilla et saisissez les informations suivantes :

   * **Hôte :** ``<nom_hôte>.local`` ou l’adresse IP du Raspberry Pi  
   * **Nom d’utilisateur :** votre nom d’utilisateur du Pi  
   * **Mot de passe :** le mot de passe défini dans Raspberry Pi Imager  
   * **Port :** ``22`` (pour SFTP)
   * Cliquez sur **Quickconnect** (ou appuyez sur **Entrée**) pour établir la connexion.

   .. image:: /_shared/appendix/img/filezilla_connect.png
      :align: center

#. Une fois connecté, le panneau de gauche affiche vos **fichiers locaux**, et le panneau de droite affiche les **fichiers du Raspberry Pi**.

    .. image:: /_shared/appendix/img/filezilla_in.png
       :align: center

#. Vous pouvez :

   * **Téléverser** un fichier : glissez du panneau gauche → panneau droit  
   * **Télécharger** un fichier : glissez du panneau droit → panneau gauche  

   FileZilla démarrera immédiatement le transfert, et l’état apparaîtra dans le panneau inférieur.
