.. _cpn_gpio_extension_board:
.. _cpn_gpio_board:

GPIO 扩展板
=====================

在开始学习命令之前，你首先需要进一步了解 Raspberry Pi 的引脚，这是后续学习的关键。

我们可以通过 GPIO 扩展板将 Raspberry Pi 的引脚轻松引出到面包板上，以避免因频繁插拔导致的 GPIO 损坏。这是我们为 Raspberry Pi 型号 B+、2 型号 B 和 3、4 型号 B 准备的 40 针 GPIO 扩展板及 GPIO 排线。

.. image:: img/image32.png
    :align: center

**引脚编号**

Raspberry Pi 的引脚有三种命名方式：wiringPi、BCM 和 Board。

在这些命名方式中，40 针 GPIO 扩展板使用的是 BCM 命名方式。但对于一些特殊引脚，如 I2C 端口和 SPI 端口，则使用其自身的名称。

下表展示了 WiringPi、Board 以及 GPIO 扩展板上每个引脚的本源名称的命名方式。例如，对于 GPIO17，Board 命名方式为 11，wiringPi 命名方式为 0，其本源名称为 GPIO0。

.. note::

    1) 在 C 语言中使用的是 WiringPi 命名方式。

    2) 在 Python 语言中，使用的命名方式是 **Board** 和 **BCM**\ ，并通过 ``GPIO.setmode()`` 函数进行设置。

    3) 在 Scratch 3 和 Processing 中，使用的命名方式是 **BCM**\ 。

.. image:: img/gpio_board.png
