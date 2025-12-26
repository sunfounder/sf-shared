
.. _install_os:

Installing the Operating System
===================================

.. start_imager

Before using your Raspberry Pi, you need to install **Raspberry Pi OS** onto a microSD card.  
This guide explains how to do that using **Raspberry Pi Imager** in a simple, beginner-friendly way.

**Required Components**

* A computer (Windows, macOS, or Linux)
* A microSD card (16GB or larger; recommended brands: SanDisk, Samsung)
* A microSD card reader

-------------------

**1. Install Raspberry Pi Imager**
-------------------------------------------

#. Visit the official Raspberry Pi Imager download page: |shared_link_rpi_imager|. Download the correct installer for your operating system.

   .. image:: /_shared/pi_start/img/imager_download.png
      :width: 70%

#. Follow the installation prompts (language, install path, confirmation). After installation, launch **Raspberry Pi Imager** from your desktop or applications menu.

   .. image:: /_shared/pi_start/img/imager_install.png
      :width: 90%

-------------------

**2. Install the OS to the microSD Card**
------------------------------------------------

#. Insert your microSD card into your computer using a card reader. Back up any important data before proceeding.

   .. image:: /_shared/pi_start/img/insert_sd.png
      :width: 90%

#. When Raspberry Pi Imager opens, you will see the **Device** page. Select your Raspberry Pi model from the list (e.g., Raspberry Pi 5, 4, 3, or Zero 2W).

   .. image:: /_shared/pi_start/img/imager_device.png
      :width: 90%

   .. end_imager

#. Go to the **OS** section and choose the recommended **Raspberry Pi OS (64-bit)** option.

   .. image:: /_shared/pi_start/img/imager_os.png
      :width: 90%

   .. start_choose_os

#. In the **Storage** section, select your microSD card. For safety, unplug other USB drives so only the SD card appears in the list.

   .. image:: /_shared/pi_start/img/imager_storage.png
      :width: 90%

#. Click **Next** to continue to the customization step.

   .. note::

      * If you will connect a monitor, keyboard, and mouse directly to your Raspberry Pi, you may click **SKIP CUSTOMISATION**.  
      * If you plan to set up the Raspberry Pi *headless* (Wi-Fi remote access), you must complete the customization settings.

   .. image:: /_shared/pi_start/img/imager_custom_skip.png
      :width: 90%

-------------------

.. _imager_custom:

**3. OS Customization Settings**
------------------------------------------

#. **Set Hostname**

   * Give your Raspberry Pi a unique hostname.  
   * You can connect to it later using ``hostname.local``.

   .. image:: /_shared/pi_start/img/imager_custom_hostname.png
      :width: 90%

#. **Set Localisation**

   * Choose your capital city.
   * Imager will auto-complete the time zone and keyboard layout based on your selection, though you can adjust them if needed. Select Next.
   
   .. image:: /_shared/pi_start/img/imager_custom_local.png
      :width: 90%

#. **Set Username & Password**

   Create a user account for your Raspberry Pi.
   
   .. image:: /_shared/pi_start/img/imager_custom_user.png
      :width: 90%

#. **Configure Wi-Fi**

   * Enter your Wi-Fi **SSID** (network name) and **password**.  
   * Your Raspberry Pi will automatically connect on first boot.
   
   .. image:: /_shared/pi_start/img/imager_custom_wifi.png
      :width: 90%

#. **Enable SSH (Optional but Recommended)**

   * Enabling SSH allows you to remotely log in from your computer.  
   * You may log in using your username/password or configure SSH keys.
   
   .. image:: /_shared/pi_start/img/imager_custom_ssh.png
      :width: 90%

#. **Enable Raspberry Pi Connect (Optional)**


   Raspberry Pi Connect allows you to access your Raspberry Pi desktop from a web browser.
   
   * Turn on **Raspberry Pi Connect**, then click **OPEN RASPBERRY PI CONNECT**.
   
     .. image:: /_shared/pi_start/img/imager_custom_connect.png
        :width: 90%

   * The Raspberry Pi Connect website will open in your default browser. Log in to your Raspberry Pi ID account, or sign up if you don’t have one yet.

     .. image:: /_shared/pi_start/img/imager_custom_open.png
        :width: 90%

   * On the **New auth key** page, create your one-time auth key. 
      
      * If your Raspberry Pi ID account isn’t part of any organisation, select **Create auth key and launch Raspberry Pi Imager**.
      * If you belong to one or more organisations, choose one, then create the key and launch Imager.
      * Make sure to power on your Raspberry Pi and connect it to the internet before the key expires.
   
     .. image:: /_shared/pi_start/img/imager_custom_authkey.png
        :width: 90%
   
   * Your browser may ask to open Raspberry Pi Imager — allow it.

     * Imager will open on the Raspberry Pi Connect tab, showing the authentication token.
     * If the token doesn’t transfer automatically, open the **Having trouble?** section on the Raspberry Pi Connect page, copy the token, and paste it into Imager manually.

     .. image:: /_shared/pi_start/img/imager_custom_connect_token.png
        :width: 90%

-------------------

**4. Write the OS Image**


#. Review all settings and click **WRITE**.

   .. image:: /_shared/pi_start/img/imager_writing.png
      :width: 90%

#. If the card already contains data, Raspberry Pi Imager will show a warning that all data on the device will be erased. Double-check that you selected the correct drive, then click **I UNDERSTAND, ERASE AND WRITE** to continue.

   .. image:: /_shared/pi_start/img/imager_erase.png
      :width: 90%

#. Wait for the writing and verification to finish. When it is done, Raspberry Pi Imager will show **Write complete!** and a summary of your choices. The storage device will be ejected automatically so you can remove it safely.


   .. image:: /_shared/pi_start/img/imager_finish.png
        :width: 90%

#. Remove the microSD card and insert it into the slot on the underside of your Raspberry Pi. Your Raspberry Pi is now ready to boot with the new OS!

   .. image:: /_shared/pi_start/img/os_sd_to_pi.jpg
        :width: 70%

   .. end_choose_os
