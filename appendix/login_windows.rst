.. note::

    Bonjour, bienvenue dans la communauté des passionnés de Raspberry Pi, Arduino et ESP32 de SunFounder sur Facebook ! Plongez dans l'univers de Raspberry Pi, Arduino et ESP32 avec d'autres passionnés.

    **Pourquoi nous rejoindre ?**

    - **Support d'experts** : Résolvez des problèmes après-vente et des défis techniques grâce à l'aide de notre communauté et de notre équipe.
    - **Apprendre et partager** : Échangez des astuces et des tutoriels pour améliorer vos compétences.
    - **Aperçus exclusifs** : Obtenez un accès anticipé aux annonces de nouveaux produits et aux avant-premières.
    - **Réductions exclusives** : Profitez de réductions spéciales sur nos derniers produits.
    - **Promotions et cadeaux festifs** : Participez à des concours et promotions festifs.

    👉 Prêt à explorer et à créer avec nous ? Cliquez sur [|link_sf_facebook|] et rejoignez-nous dès aujourd'hui !

.. _login_windows:

PuTTY
=========================

PuTTY est un client SSH simple et fiable pour les utilisateurs Windows, permettant d’accéder à distance au Raspberry Pi.  


.. |shared_link_putty| raw:: html

    <a href="https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html>" target="_blank">PuTTY</a> 


#. Téléchargez PuTTY depuis |shared_link_putty| et installez-le sur votre ordinateur.

   .. image:: /_shared/appendix/img/putty_download.png
      :width: 70%


#. Ouvrez PuTTY et préparez la connexion :

   * Saisissez le **nom d’hôte ou l’adresse IP** de votre Raspberry Pi dans **Host Name**.
   * Définissez le **Port** sur ``22``.
   * Cliquez sur **Open** pour vous connecter.


   .. image:: /_shared/appendix/img/putty_open.png
      :width: 70%
   
#. Si un avertissement de sécurité apparaît lors de la première utilisation, cliquez sur **Accept** pour continuer.

   .. image:: /_shared/appendix/img/putty_accept.png
      :width: 70%

#. Connectez-vous au Raspberry Pi :

   * Lorsque **login as:** s’affiche, saisissez le nom d’utilisateur que vous avez défini dans **Raspberry Pi Imager**.
   * Entrez votre mot de passe (il ne s’affichera pas pendant la saisie — c’est normal).
   * Après la connexion, le terminal est prêt pour que vous puissiez entrer des commandes et utiliser votre Raspberry Pi à distance.

   .. image:: /_shared/appendix/img/putty_login.png
      :width: 70%

.. note::

    Si PuTTY affiche **inactive**, la connexion a été perdue et doit être rétablie.
