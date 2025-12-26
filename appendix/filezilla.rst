
.. _filezilla:

FileZilla Software
==================

.. image:: /_shared/appendix/img/filezilla_icon.png
   :width: 20%

File Transfer Protocol (FTP) is commonly used to transfer files between computers over a network.  
**FileZilla** is an open-source client that supports FTP, FTPS, and **SFTP** (recommended for Raspberry Pi).  
With FileZilla, you can easily upload files (such as images, audio, and scripts) from your computer to the Raspberry Pi, or download files from the Pi back to your computer.

Download FileZilla
------------------

#. Visit the |shared_link_filezilla| official website and download **FileZilla Client** for your operating system.

#. Install and launch the program.

   .. image:: /_shared/appendix/img/filezilla_install.png

#. Open FileZilla and enter the following information:

   * **Host:** ``<hostname>.local`` or the Raspberry Pi’s IP address  
   * **Username:** your Pi username  
   * **Password:** the password set in Raspberry Pi Imager  
   * **Port:** ``22`` (for SFTP)
   * Click **Quickconnect** (or press **Enter**) to establish a connection.

   .. image:: /_shared/appendix/img/filezilla_connect.png
      :align: center

#. Once connected, the left panel shows your **local files**, and the right panel shows the **Raspberry Pi files**.

    .. image:: /_shared/appendix/img/filezilla_in.png
       :align: center

#. You can:

   * **Upload** a file: drag from the left panel → right panel  
   * **Download** a file: drag from the right panel → left panel  

   FileZilla will immediately start the transfer, and the status will appear in the panel at the bottom.
