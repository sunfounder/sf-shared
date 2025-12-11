.. note::

    Hallo und willkommen in der SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasten-Gemeinschaft auf Facebook! Tauchen Sie tiefer ein in die Welt von Raspberry Pi, Arduino und ESP32 mit anderen Enthusiasten.

    **Warum beitreten?**

    - **Expertenunterstützung**: Lösen Sie Nachverkaufsprobleme und technische Herausforderungen mit Hilfe unserer Gemeinschaft und unseres Teams.
    - **Lernen & Teilen**: Tauschen Sie Tipps und Anleitungen aus, um Ihre Fähigkeiten zu verbessern.
    - **Exklusive Vorschauen**: Erhalten Sie frühzeitigen Zugang zu neuen Produktankündigungen und exklusiven Einblicken.
    - **Spezialrabatte**: Genießen Sie exklusive Rabatte auf unsere neuesten Produkte.
    - **Festliche Aktionen und Gewinnspiele**: Nehmen Sie an Gewinnspielen und Feiertagsaktionen teil.

    👉 Sind Sie bereit, mit uns zu erkunden und zu erschaffen? Klicken Sie auf [|link_sf_facebook|] und treten Sie heute bei!

.. _login_windows:

PuTTY
=========================

PuTTY ist ein einfacher und zuverlässiger SSH-Client für Windows-Benutzer, um remote auf den Raspberry Pi zuzugreifen.

#. Laden Sie PuTTY von |shared_link_putty| herunter und installieren Sie es auf Ihrem Computer.

   .. image:: /_shared/appendix/img/putty_download.png
      :width: 70%


#. Öffnen Sie PuTTY und bereiten Sie die Verbindung vor:

   * Geben Sie den **Hostnamen oder die IP-Adresse** Ihres Raspberry Pi in **Host Name** ein.
   * Setzen Sie den **Port** auf ``22``.
   * Klicken Sie auf **Open**, um die Verbindung herzustellen.


   .. image:: /_shared/appendix/img/putty_open.png
      :width: 70%
   
#. Wenn beim ersten Start eine Sicherheitswarnung erscheint, klicken Sie auf **Accept**, um fortzufahren.

   .. image:: /_shared/appendix/img/putty_accept.png
      :width: 70%

#. Melden Sie sich beim Raspberry Pi an:

   * Wenn **login as:** erscheint, geben Sie den Benutzernamen ein, den Sie im **Raspberry Pi Imager** festgelegt haben.
   * Geben Sie Ihr Passwort ein (es wird während der Eingabe nicht angezeigt—das ist normal).
   * Nach erfolgreicher Anmeldung ist das Terminal bereit, Befehle einzugeben und den Raspberry Pi fernzusteuern.

   .. image:: /_shared/appendix/img/putty_login.png
      :width: 70%

.. note::

    Wenn PuTTY **inactive** anzeigt, wurde die Verbindung getrennt und muss erneut hergestellt werden.
