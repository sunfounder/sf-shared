.. note::

    Bonjour et bienvenue dans la Communauté Facebook des passionnés de Raspberry Pi, Arduino et ESP32 de SunFounder ! Plongez plus profondément dans l'univers des Raspberry Pi, Arduino et ESP32 avec d'autres passionnés.

    **Pourquoi rejoindre ?**

    - **Support d'experts** : Résolvez les problèmes après-vente et les défis techniques avec l'aide de notre communauté et de notre équipe.
    - **Apprendre et partager** : Échangez des astuces et des tutoriels pour améliorer vos compétences.
    - **Aperçus exclusifs** : Accédez en avant-première aux annonces de nouveaux produits et aux aperçus.
    - **Réductions spéciales** : Profitez de réductions exclusives sur nos produits les plus récents.
    - **Promotions festives et cadeaux** : Participez à des cadeaux et des promotions de vacances.

    👉 Prêt à explorer et à créer avec nous ? Cliquez [|link_sf_facebook|] et rejoignez-nous aujourd'hui !


Matrice LED à points
======================

.. image:: img/matrix_pic.png
    :width: 300

La matrice LED à points peut être divisée en deux types : **Cathode commune (CC)** et **Anode commune (CA)**.  
Elles se ressemblent extérieurement, mais leur structure électrique interne est différente.

La matrice LED utilisée dans ce kit est de type **Anode commune (CA)**.  
Vous pouvez l’identifier grâce au marquage **« 788BS »** imprimé sur le côté du module.

Disposition des broches
----------------------------------------

Les broches sont situées des deux côtés à l’arrière du module.  
Lorsque vous faites face au côté portant l’étiquette :

* Les broches **1–8** se trouvent d’un côté  
* Les broches **9–16** se trouvent du côté opposé  

Vue externe :

.. image:: img/matrix_pin.png

Structure interne
-----------------------

La figure suivante montre la structure interne de la matrice LED à points.

* Dans une matrice **Anode commune (CA)**, **ROW = Anode** et **COL = Cathode**
* Dans une matrice **Cathode commune (CC)**, **ROW = Cathode** et **COL = Anode**

.. image:: img/matrix_internal.png
   :width: 400
   :align: center

Pour les types CA et CC, la position physique des broches de lignes et de colonnes est identique — seule la polarité électrique diffère.

Correspondance des broches
--------------------------------------

.. list-table::
   :header-rows: 2
   :align: center

   * - **COL**
     - **1**
     - **2**
     - **3**
     - **4**
     - **5**
     - **6**
     - **7**
     - **8**
   * - **Broche n°**
     - **13**
     - **3**
     - **4**
     - **10**
     - **6**
     - **11**
     - **15**
     - **16**
   * - **ROW**
     - **1**
     - **2**
     - **3**
     - **4**
     - **5**
     - **6**
     - **7**
     - **8**
   * - **Broche n°**
     - **9**
     - **14**
     - **8**
     - **12**
     - **1**
     - **7**
     - **2**
     - **5**

Comment les LED sont allumées
--------------------------------------------

Pour contrôler une LED individuelle, vous devez activer correctement ses broches **ROW** et **COL**.

*Exemple : LED en haut à gauche (ROW 1, COL 1)*

- **Type CA**  
  Définir **ROW broche 9 = High**, **COL broche 13 = Low**

- **Type CC**  
  Définir **COL broche 13 = High**, **ROW broche 9 = Low**

*Exemple : allumer toute la première colonne*

- **Type CA**  
  Définir **COL broche 13 = Low**  
  Définir **ROW broches 9, 14, 8, 12, 1, 7, 2, 5 = High**

- **Type CC**  
  Définir **COL broche 13 = High**  
  Définir **ROW broches 9, 14, 8, 12, 1, 7, 2, 5 = Low**

Cette méthode de balayage lignes-colonnes permet de contrôler chaque LED individuellement à l’aide du multiplexage.
