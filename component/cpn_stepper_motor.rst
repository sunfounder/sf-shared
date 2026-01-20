.. note::

    Hallo und willkommen in der SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasten-Gemeinschaft auf Facebook! Tauchen Sie tiefer ein in die Welt von Raspberry Pi, Arduino und ESP32 mit anderen Enthusiasten.

    **Warum beitreten?**

    - **Expertenunterstützung**: Lösen Sie Nachverkaufsprobleme und technische Herausforderungen mit Hilfe unserer Gemeinschaft und unseres Teams.
    - **Lernen & Teilen**: Tauschen Sie Tipps und Anleitungen aus, um Ihre Fähigkeiten zu verbessern.
    - **Exklusive Vorschauen**: Erhalten Sie frühzeitigen Zugang zu neuen Produktankündigungen und exklusiven Einblicken.
    - **Spezialrabatte**: Genießen Sie exklusive Rabatte auf unsere neuesten Produkte.
    - **Festliche Aktionen und Gewinnspiele**: Nehmen Sie an Gewinnspielen und Feiertagsaktionen teil.

    👉 Sind Sie bereit, mit uns zu erkunden und zu erschaffen? Klicken Sie auf [|link_sf_facebook|] und treten Sie heute bei!


Schrittmotor und ULN2003-Modul
=========================================

**Schrittmotor**

Der 28BYJ-48 ist ein 5-adriger unipolarer Schrittmotor, der mit 5 V betrieben wird. Schrittmotoren sind Präzisionsmotoren, die sehr genau gesteuert werden können, ohne dass eine Rückmeldung durch Sensoren erforderlich ist. Dies liegt daran, dass die Motorwelle mit Magneten ausgestattet ist und durch elektromagnetische Spulen gesteuert wird, die in einer bestimmten Reihenfolge ein- und ausgeschaltet werden und die Welle in präzisen kleinen Schritten bewegen.

.. image:: img/step_stepper.png
  :align: center

Der Stator des von uns verwendeten Schrittmotors besitzt 32 magnetische Pole, sodass für eine vollständige Umdrehung 32 Schritte erforderlich sind. Die Abtriebswelle des Schrittmotors ist mit einem Untersetzungsgetriebe verbunden, wobei das Untersetzungsverhältnis 1/64 beträgt. Daher benötigt die endgültige Abtriebswelle für eine vollständige Umdrehung 32 × 64 = 2048 Schritte.

**Funktionsweise eines unipolaren Schrittmotors**

Ein unipolarer Schrittmotor besitzt in der Regel vier Phasen und wird mit Gleichstrom betrieben. Durch die korrekte zeitliche Ansteuerung des elektrischen Stroms zu den einzelnen Phasen des Motors kann dieser schrittweise rotieren. Stellen Sie sich vor, dass sich im Zentrum des Motors ein zahnradförmiger Magnet (der Rotor) befindet, der von mehreren Zähnen mit den Nummern 0 bis 5 umgeben ist. Um diese Zähne herum befinden sich acht magnetische Pole, die paarweise (A bis D) angeordnet und durch Spulen verbunden sind.

.. image:: img/step_interal.png
  :align: center

Wenn Sie verschiedene Schalter einschalten, die mit diesen Spulen verbunden sind (bezeichnet als SA, SB, SC und SD), steuern Sie, welche magnetischen Pole aktiviert werden. Wenn zum Beispiel der Schalter SB eingeschaltet ist (und die anderen ausgeschaltet sind), richten sich die magnetischen Pole B an bestimmten Zähnen des Rotors aus und bewirken eine Bewegung. Wenn anschließend der Schalter SC eingeschaltet wird, dreht sich der Rotor weiter, um sich an den magnetischen Polen C auszurichten, und so weiter. Durch zyklisches Aktivieren der Schalter A, B, C und D rotiert der Rotor kontinuierlich.

**ULN2003-Modul**

.. image:: img/step_uln2003.png
    :align: center

Das ULN2003-Schrittmotor-Treibermodul ist entscheidend für die Integration des Schrittmotors in eine Schaltung. Es arbeitet als 7-Kanal-Inverter, was bedeutet, dass es Eingangssignale in die für den Motor erforderlichen Ausgangsaktionen umwandelt. Wenn beispielsweise ein High-Signal an IN1 und Low-Signale an IN2, IN3 und IN4 angelegt werden, wird OUT1 auf Low geschaltet, während die anderen Ausgänge auf High bleiben, wodurch sich der Motor um einen Schritt dreht. Durch das Bereitstellen solcher spezifischen Sequenzen kann sich der Motor gleichmäßig Schritt für Schritt drehen. Der ULN2003 vereinfacht die Steuerung der für den Motorbetrieb notwendigen Zeitabläufe erheblich.
