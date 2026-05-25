.. _cpn_avoid_module:

避障模块
=========

.. image:: img/2.2.5IR_Obstacle.png
   :width: 400
   :align: center

红外避障模块对环境光有较强的适应能力，它带有一对红外发射和接收管。

发射管发射红外频率，当检测方向遇到障碍物时，红外辐射被接收管接收，
经过比较器电路处理后，绿色指示灯会亮起并输出低电平信号。

检测距离可通过电位器调节，有效距离范围为 2-30cm。

.. image:: img/IR_module.png
    :width: 600
    :align: center

.. **Example**

.. * :ref:`2.2.5_c` (C Project)
.. * :ref:`2.2.5_py` (Python Project)
.. * :ref:`1.11_scratch` (Scratch Project)
