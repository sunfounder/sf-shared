.. _cpn_circular_ws2812_module:

Module LED WS2812 circulaire
===========================================================

.. image:: img/c_ws2812_module.png
    :width: 40%
    :align: center

Ce module LED WS2812 circulaire contient 12 LED RGB adressables individuellement, chacune avec un pilote intégré prenant en charge un contrôle des couleurs sur 24 bits via une seule ligne de données. Le module expose quatre broches — VCC, GND, DIN et DOUT — pour une connexion facile aux contrôleurs tels que Raspberry Pi ou Arduino.

**Aperçu des broches**

* **V (VCC)** : Entrée d'alimentation 5 V. Assurez-vous que votre alimentation peut fournir suffisamment de courant pour toutes les LED.
* **G (GND)** : Masse. Doit être partagée avec votre contrôleur pour une signalisation correcte.
* **R (DIN)** : Reçoit les données de votre microcontrôleur. C'est l'entrée de commande.
* **D (DOUT)** : Envoie les données aux anneaux ou bandes LED supplémentaires, permettant une extension en guirlande (daisy-chain).

**Utilisation**

Les LED se transmettent les données de l'une à l'autre, permettant un contrôle indépendant de chaque LED et autorisant des effets tels que les balayages de couleur, les dégradés, les rotations et les motifs d'animation.
Cet anneau compact de 12 LED convient aux indicateurs, à l'éclairage décoratif, à la robotique, aux dispositifs portables, aux horloges et aux petits projets d'affichage.
