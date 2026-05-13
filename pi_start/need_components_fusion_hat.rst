.. note::

    Bonjour, bienvenue dans la communauté des passionnés de Raspberry Pi, Arduino et ESP32 de SunFounder sur Facebook ! Plongez dans l'univers de Raspberry Pi, Arduino et ESP32 avec d'autres passionnés.

    **Pourquoi nous rejoindre ?**

    - **Support d'experts** : Résolvez les problèmes après-vente et les défis techniques avec l'aide de notre communauté et de notre équipe.
    - **Apprendre et partager** : Échangez des conseils et des tutoriels pour améliorer vos compétences.
    - **Aperçus exclusifs** : Accédez en avant-première aux annonces de nouveaux produits et à des aperçus exclusifs.
    - **Réductions spéciales** : Profitez de réductions exclusives sur nos nouveaux produits.
    - **Promotions et cadeaux festifs** : Participez à des concours et à des promotions festives.

    👉 Prêt à explorer et à créer avec nous ? Cliquez sur [|link_sf_facebook|] et rejoignez-nous dès aujourd'hui !

.. start_need_components_fusion_hat

De quoi avez-vous encore besoin ?
=============================================

Avant de commencer à utiliser ce kit, préparons le matériel essentiel.

Composants requis
------------------------------

* **Raspberry Pi**

  Le Raspberry Pi agit comme le **cerveau**, prenant en charge toutes les tâches de calcul, de détection et de contrôle.  
  
  .. image:: /_shared/pi_start/img/need_pi.jpg

  * **Modèles compatibles** : Raspberry Pi 5, Raspberry Pi 4, 3 ou Raspberry Pi Zero 2W  
  * **Minimum** : **2 Go de RAM** — suffisant pour tous les projets Python standard et pour l’utilisation de **services d’IA en ligne** tels que OpenAI Whisper, TTS ou les LLM.  
  * **Recommandé** : **4 Go de RAM ou plus** — garantit des performances plus fluides lors de l’exécution de **modèles d’IA locaux** (par exemple la reconnaissance vocale Vosk, Piper TTS ou des LLM légers), en parallèle du streaming caméra et des tâches de contrôle.  
  

* **Adaptateur d’alimentation**

  Ce kit est fourni avec un **pack de batteries 18650** et une carte **Fusion HAT+** intégrant un circuit de charge.
  
  .. image:: /_shared/pi_start/img/need_power.png
    :width: 400

  * Pour la charge, il est recommandé d’utiliser une **alimentation 5 V 3 A**, telle que l’**adaptateur USB-C officiel Raspberry Pi 15 W**.  
  * Vous pouvez également utiliser un **chargeur USB-C Power Delivery (PD)** ou un **chargeur rapide QC 2.0**.  
  * Une charge complète prend généralement environ **2 heures** (de 0 % à 100 %).  


* **Carte microSD**

  Le Raspberry Pi ne dispose pas de disque dur intégré. Il démarre et stocke tous les fichiers sur une **carte microSD**.  
  
  .. image:: /_shared/pi_start/img/need_sd.jpg
    :width: 200

  * Minimum : **16 Go**  
  * Recommandé : **32 Go** pour une meilleure stabilité  
  * Marque : utilisez des options fiables telles que **SanDisk** ou **Samsung** afin d’éviter les erreurs de lecture/écriture  
  

Composants optionnels
------------------------

Bien que non strictement indispensables, les périphériques suivants amélioreront grandement votre expérience d’apprentissage et de débogage :

* **Écran (HDMI ou TV)** 

  Pour les débutants, nous recommandons vivement un écran disposant d’une entrée HDMI, afin de pouvoir configurer facilement Raspberry Pi OS et exécuter des programmes graphiques.  

  .. image:: /_shared/pi_start/img/need_screen.png
    :width: 400

* **Câble HDMI (standard / mini / micro)**
 
  Les différents modèles de Raspberry Pi utilisent différents connecteurs HDMI. Assurez-vous de vérifier votre modèle de Pi et de préparer le câble approprié. 
  
  * **Raspberry Pi 4 / 5** : Micro HDMI  
  * **Raspberry Pi 3** : HDMI standard  
  * **Raspberry Pi Zero 2W** : Mini HDMI  

  .. image:: /_shared/pi_start/img/need_hdmi.png
    :width: 400

* **Clavier et souris**

  Très utiles lors de la configuration initiale de Raspberry Pi OS. Par la suite, vous pourrez passer à un accès à distance (SSH/VNC), mais pour les débutants, nous recommandons de prévoir un ensemble USB ou sans fil de base.  

  .. image:: /_shared/pi_start/img/need_keyboard_mouse.png
    :width: 500
 

**Conseils de préparation**

* Si vous avez acheté ce kit, la plupart des accessoires sont inclus, mais vous devez tout de même préparer séparément la carte Raspberry Pi, la carte microSD et l’adaptateur d’alimentation.  
* Vous ne savez pas quoi acheter ? Le choix le plus stable et universel est : **Raspberry Pi 4 (2 Go) + alimentation officielle + carte microSD de 32 Go**.

.. end_need_components_fusion_hat
