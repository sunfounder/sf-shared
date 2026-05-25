.. _cpn_thermistor:

热敏电阻
===============

.. image:: img/thermistor.png
    :width: 150
    :align: center

热敏电阻是一种电阻值随温度变化而显著变化的电阻器，其变化幅度远大于普通电阻器。"Thermistor"一词由 thermal（热）和 resistor（电阻）组合而成。热敏电阻广泛用作浪涌电流限制器、温度传感器（通常为负温度系数 NTC 型）、自恢复过流保护器和自调节加热元件（通常为正温度系数 PTC 型）。

* `Thermistor - Wikipedia <https://en.wikipedia.org/wiki/Thermistor>`_

以下是热敏电阻的电路符号。

.. image:: img/thermistor_symbol.png
    :width: 300
    :align: center

热敏电阻分为两种相反的基本类型：

* **NTC 热敏电阻**\ ：电阻值随温度升高而降低，通常是由于热激发使价带中的导电电子增多。NTC 常用作温度传感器，或串联在电路中用作浪涌电流限制器。
* **PTC 热敏电阻**\ ：电阻值随温度升高而增大，通常是由于晶格热振动加剧，特别是杂质和缺陷引起的振动。PTC 通常串联在电路中，用作可恢复保险丝，用于过流保护。

本套件中使用的是 NTC 热敏电阻。每个热敏电阻都有一个标称电阻值。此处为 10kΩ，在 25°C 条件下测得。

以下是电阻值与温度之间的关系：

    RT = RN * expB(1/TK – 1/TN)

* **RT**\ 为温度 TK 时 NTC 热敏电阻的电阻值。
* **RN**\ 为额定温度 TN 下 NTC 热敏电阻的电阻值。此处 RN 的数值为 10k。
* **TK**\ 为开尔文温度，单位为 K。此处 TK 的数值为 273.15 + 摄氏度。
* **TN**\ 为额定开尔文温度，单位也为 K。此处 TN 的数值为 273.15+25。
* **B(beta)**\ 为 NTC 热敏电阻的材料常数，也称为热敏指数，数值为 3950。
* **exp**\ 为指数（exponential）的缩写，底数 e 为自然常数，约等于 2.7。

将公式转换为 TK=1/(ln(RT/RN)/B+1/TN)，得到开尔文温度，减去 273.15 即为摄氏度。

该关系为经验公式，仅在温度和电阻值处于有效范围内时准确。

.. **Example**

.. * :ref:`2.2.2_c` (C Project)
.. * :ref:`3.1.4_c` (C Project)
.. * :ref:`3.1.7_c` (C Project)
.. * :ref:`2.2.2_py` (Python Project)
.. * :ref:`4.1.10_py` (Python Project)
.. * :ref:`4.1.13_py` (Python Project)
