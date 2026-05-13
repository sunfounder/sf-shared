.. note::

    Bonjour et bienvenue dans la Communauté Facebook des passionnés de Raspberry Pi, Arduino et ESP32 de SunFounder ! Plongez plus profondément dans l'univers des Raspberry Pi, Arduino et ESP32 avec d'autres passionnés.

    **Pourquoi rejoindre ?**

    - **Support d'experts** : Résolvez les problèmes après-vente et les défis techniques avec l'aide de notre communauté et de notre équipe.
    - **Apprendre et partager** : Échangez des astuces et des tutoriels pour améliorer vos compétences.
    - **Aperçus exclusifs** : Accédez en avant-première aux annonces de nouveaux produits et aux aperçus.
    - **Réductions spéciales** : Profitez de réductions exclusives sur nos produits les plus récents.
    - **Promotions festives et cadeaux** : Participez à des cadeaux et des promotions de vacances.

    👉 Prêt à explorer et à créer avec nous ? Cliquez [|link_sf_facebook|] et rejoignez-nous aujourd'hui !

.. _cpn_motor_xh254:

Moteur CC XH2.54
===================

.. image:: img/motor_254_pic.png
    :width: 50%
    :align: center

Un moteur à courant continu (CC) est un actionneur électrique simple qui convertit l'énergie électrique en rotation mécanique.
Il est largement utilisé dans des dispositifs tels que les pompes, les ventilateurs, les compresseurs et les petits robots grâce à sa capacité à fournir un mouvement rotatif continu.

**Spécifications du moteur**

* **Tension de fonctionnement** : 3–5 V
* **Courant à vide (3 V)** : 100–120 mA
* **Vitesse à vide (3 V)** : 8000 tr/min
* **Couple de blocage (3 V)** : 140 g·cm
* **Courant de blocage (3 V)** : 650 mA
* **Type de connecteur** : XH2.54 2P (blanc)
* **Longueur des fils** : Rouge/Noir, 10 cm, 24 AWG
* **Dimensions** : 25 × 20 × 15 mm

Un moteur CC se compose de deux éléments principaux : le **stator**, qui reste fixe, et le **rotor** (ou **induit**), qui tourne pour générer le mouvement.
Le rotor est placé dans un champ magnétique créé par des aimants permanents. Lorsque le courant traverse les enroulements de l'induit, il produit un champ magnétique qui interagit avec le champ du stator, générant un couple qui provoque la rotation.

.. image:: img/motor_sche.png
    :align: center

Le courant circule de l'alimentation vers les balais, puis dans le collecteur, et enfin vers les enroulements de l'induit.
Le collecteur inverse périodiquement le sens du courant à chaque demi-tour, garantissant que le couple agit toujours dans la direction correcte pour maintenir une rotation continue.
Cette action de commutation convertit efficacement l'alimentation CC en une forme de courant alternatif à l'intérieur du moteur, permettant un mouvement fluide et soutenu.
