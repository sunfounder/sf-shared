.. _cpn_led:

LED
==========

.. image:: img/LED.png
    :width: 400

半导体发光二极管是一种通过 PN 结将电能转化为光能的元件。按波长可分为激光二极管、红外发光二极管和可见光发光二极管，后者通常被称为发光二极管（LED）。

二极管具有单向导电性，因此电流方向将如电路符号中箭头所示。你只能将正极接正电源，负极接负电源，这样 LED 才会发光。

.. image:: img/led_symbol.png


LED 有两个引脚。长引脚为正极，短引脚为负极。注意不要接反。LED 具有固定的正向压降，因此不能直接接入电路，因为电源电压可能超过该压降导致 LED 烧毁。红色、黄色和绿色 LED 的正向压降为 1.8V，白色 LED 为 2.6V。大多数 LED 能承受的最大电流为 20mA，因此需要串联一个限流电阻。

电阻值的计算公式如下：

    R = (Vsupply – VD)/I

**R** 表示限流电阻的阻值，**Vsupply** 表示电源电压，**VD** 表示压降，**I** 表示 LED 的工作电流。

以下是 LED 的详细介绍：`LED - Wikipedia <https://en.wikipedia.org/wiki/Light-emitting_diode>`_.

.. **Example**

.. * :ref:`1.1.1_c` (C Project)
.. * :ref:`3.1.6_c` (C Project)
.. * :ref:`1.1.1_py` (Python Project)
.. * :ref:`4.1.12_py` (Python Project)
.. * :ref:`1.1_scratch` (Scratch Project)
