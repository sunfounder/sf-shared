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

PuTTY ist ein einfacher und zuverlässiger SSH-Client für Windows-Nutzer, mit dem Sie aus der Ferne auf den Raspberry Pi zugreifen können.  


.. |shared_link_putty| raw:: html

    <a href="https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html" target="_blank">PuTTY</a> 


#. Laden Sie PuTTY von |shared_link_putty| herunter und installieren Sie es auf Ihrem Computer.

   .. image:: /_shared/appendix/img/putty_download.png
      :width: 70%


#. Öffnen Sie PuTTY und bereiten Sie die Verbindung vor:

   * Geben Sie den **Hostname oder die IP-Adresse** Ihres Raspberry Pi im Feld **Host Name** ein.
   * Setzen Sie den **Port** auf ``22``.
   * Klicken Sie auf **Open**, um die Verbindung herzustellen.


   .. image:: /_shared/appendix/img/putty_open.png
      :width: 70%
   
#. Wenn beim ersten Start eine Sicherheitswarnung erscheint, klicken Sie auf **Accept**, um fortzufahren.

   .. image:: /_shared/appendix/img/putty_accept.png
      :width: 70%

#. Melden Sie sich am Raspberry Pi an:

   * Wenn **login as:** angezeigt wird, geben Sie den Benutzernamen ein, den Sie im **Raspberry Pi Imager** festgelegt haben.
   * Geben Sie Ihr Passwort ein (es wird während der Eingabe nicht angezeigt – das ist normal).
   * Nach der Anmeldung ist das Terminal bereit, und Sie können Befehle eingeben und Ihren Raspberry Pi aus der Ferne bedienen.

   .. image:: /_shared/appendix/img/putty_login.png
      :width: 70%

.. note::

    Wenn PuTTY **inactive** anzeigt, wurde die Verbindung getrennt und muss erneut hergestellt werden.
