.. _cpn_camera_module:

摄像头模块
==========

**描述**

.. image:: img/camera_module_pic.png
   :width: 200
   :align: center

这是一款 5MP Raspberry Pi 摄像头模块，采用 OV5647 传感器。即插即用，将附带的排线连接到 Raspberry Pi 的 CSI（摄像头串行接口）端口即可使用。

该电路板尺寸小巧，约 25mm x 23mm x 9mm，重 3g，非常适合移动或其他对尺寸和重量有严格要求的应用。摄像头模块原生分辨率为 5 百万像素，配备板载定焦镜头，可拍摄 2592 x 1944 像素的静态图像，同时支持 1080p30、720p60 和 640x480p90 视频。

.. note::

   该模块仅能拍摄图片和视频，不支持录音。

**规格**

* **静态图像分辨率**\ ：2592×1944
* **支持视频分辨率**\ ：1080p/30 fps、720p/60fps 和 640 x480p 60/90 视频录制
* **光圈（F）**\ ：1.8
* **视角**\ ：65 度
* **尺寸**\ ：24mmx23.5mmx8mm
* **重量**\ ：3g
* **接口**\ ：CSI 接口
* **支持操作系统**\ ：Raspberry Pi OS（建议使用最新版本）

**安装摄像头模块**
-------------------------------------

在摄像头模块或 Raspberry Pi 上，您会找到一个扁平塑料连接器。小心地向外拉出黑色固定卡扣，直至其部分拉出。按照图示方向将 FFC 排线插入塑料连接器，然后将固定卡扣推回原位。

如果 FFC 排线安装正确，它会保持平直，轻轻拉动时不会脱出。如果没有，请重新安装。

.. image:: img/connect_ffc.png
.. image:: img/1.10_camera.png
   :width: 700

.. warning::

   请勿在通电状态下安装摄像头，否则可能损坏摄像头。

.. **Example**

.. * :ref:`3.1.1_py` (Python Project)
.. * :ref:`3.1.2_py` (Python Project)
.. * :ref:`4.1.1_py` (Python Project)
.. * :ref:`4.1.4_py` (Python Project)
.. * :ref:`4.1.5_py` (Python Project)
.. * :ref:`1.10_scratch` (Scratch Project)
.. * :ref:`1.18_scratch` (Scratch Project)
