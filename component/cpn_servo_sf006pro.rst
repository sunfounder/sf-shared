.. note::

    Bonjour et bienvenue dans la Communauté Facebook des passionnés de Raspberry Pi, Arduino et ESP32 de SunFounder ! Plongez plus profondément dans l'univers des Raspberry Pi, Arduino et ESP32 avec d'autres passionnés.

    **Pourquoi rejoindre ?**

    - **Support d'experts** : Résolvez les problèmes après-vente et les défis techniques avec l'aide de notre communauté et de notre équipe.
    - **Apprendre et partager** : Échangez des astuces et des tutoriels pour améliorer vos compétences.
    - **Aperçus exclusifs** : Accédez en avant-première aux annonces de nouveaux produits et aux aperçus.
    - **Réductions spéciales** : Profitez de réductions exclusives sur nos produits les plus récents.
    - **Promotions festives et cadeaux** : Participez à des cadeaux et des promotions de vacances.

    👉 Prêt à explorer et à créer avec nous ? Cliquez [|link_sf_facebook|] et rejoignez-nous aujourd'hui !

.. _cpn_sf006pro_servo:

Servo SF006PRO
===================

.. image:: img/servo_metal.png
    :width: 50%
    :align: center

Ce servo est un actionneur petit et fiable qui fonctionne sur 4–6 V, offrant un mouvement fluide et jusqu'à 180° de contrôle. Il fournit un bon couple, une réponse rapide et une faible consommation d'énergie, ce qui le rend adapté à la robotique, aux mécanismes et aux projets de loisirs en général.
Son interface PWM standard à 3 broches facilite la connexion aux microcontrôleurs tels qu'Arduino ou Raspberry Pi.

**Fonctionnement d'un servo**


Un servo typique se compose de plusieurs composants internes :

* Boîtier
* Arbre de sortie
* Système d'engrenages
* Potentiomètre
* Moteur CC
* Carte de commande (intégrée)

Le microcontrôleur envoie des signaux de commande PWM au servo via la broche de signal.
La carte de commande interprète le signal et pilote le moteur CC, qui fait tourner le système d'engrenages. Après avoir traversé le système de réduction à engrenages, l'arbre tourne avec un couple accru.

L'arbre de sortie est mécaniquement relié au potentiomètre. Lorsque l'arbre tourne, le potentiomètre modifie sa tension de sortie. La carte de commande lit ce retour pour déterminer la position actuelle, ajustant la rotation du moteur jusqu'à ce que l'arbre atteigne et maintienne l'angle cible.

.. image:: img/servo_internal.png
    :align: center

**Commande PWM**

L'angle de rotation du servo est déterminé par la largeur de l'impulsion PWM. Le servo attend normalement une impulsion toutes les **20 ms**.

Comportement typique des impulsions :

* **1,5 ms** → Position neutre (environ 90°)
* **< 1,5 ms** → Déplacement dans le sens antihoraire depuis le centre
* **> 1,5 ms** → Déplacement dans le sens horaire depuis le centre

La plupart des servos de loisirs acceptent des largeurs d'impulsion entre **0,5 ms et 2,5 ms**, correspondant à leur plage de mouvement complète.

.. image:: img/servo_duty.png
    :width: 600
    :align: center


**Paramètres**

.. list-table::
   :header-rows: 1
   :widths: 25 75

   * - Paramètre
     - Spécification

   * - Tension de fonctionnement
     - CC 4 V–6 V (nominale 5 V, recommandé d'utiliser une alimentation 5 V)

   * - Courant de veille
     - ≤ 5 mA

   * - Courant à vide
     - ≤ 350 mA à 5 V (pic mesuré manuellement)

   * - Courant de blocage
     - ≤ 1,2 A à 5 V (tombe à ≤ 250 mA après 5 secondes de blocage)

   * - Couple nominal
     - 0,75 kgf·cm (à 5 V)

   * - Charge dynamique maximale
     - ≥ 2,2 kgf·cm (à 5 V)

   * - Couple de blocage (statique)
     - ≥ 5 kgf·cm (testé au couplemètre)

   * - Vitesse à vide
     - ≤ 0,17 sec/60° (à 5 V)

   * - Angle de débattement
     - 90° ±10° (1000–2000 μs)

   * - Angle de fonctionnement maximal
     - 180° ±10° (500–2500 μs)

   * - Angle limite mécanique
     - 360°

   * - Plage de largeur d'impulsion
     - 500 μs ~ 2500 μs

   * - Position neutre
     - 1500 μs

   * - Largeur de bande morte
     - ≤ 6 μs

   * - Jeu mécanique
     - ≤ 0,5°

   * - Poids
     - 13,5 ± 0,5 g

   * - Matériau des engrenages
     - Engrenages hybrides plastique + métal

   * - Type de moteur
     - Moteur à noyau de fer

   * - Type de potentiomètre
     - Film de carbone, angle 220°, ≥ 100 000 cycles

   * - Câble
     - 250 ±5 mm, connecteur JR 3 broches (Marron–Rouge–Orange)

   * - Brochage du connecteur
     - Orange : Signal PWM

       Rouge : VCC

       Marron : GND

   * - Interface de communication
     - PWM

       Tension du signal : HAUT 2,0–5,0 V / BAS 0,0–0,6 V

       Fréquence de trame : 3–30 ms (par défaut 20 ms)

       Plage d'impulsion : 500–2500 μs

**Dimensions**

.. image:: img/servo_metal_size.png
    :width: 80%
    :align: center
