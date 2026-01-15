Stepper Motor and ULN2003 Module
=========================================

**Stepper Motor**

The 28BYJ-48 is a 5-wire unipolar stepper motor that operates at 5V. Stepper motors are precision motors that can be controlled very accurately without needing feedback from sensors. This is because the motor's shaft is equipped with magnets and controlled by electromagnetic coils that turn on and off in a specific sequence, moving the shaft in precise small steps.

.. image:: img/step_stepper.png
  :align: center

The stator of Stepper Motor we use has 32 magnetic poles, so a circle needs 32 steps. The output shaft of the Stepper Motor is connected with a reduction gear set, and the reduction ratio is 1/64. So the final output shaft rotates a circle requiring a 32*64=2048 step.

**How a Unipolar Stepper Motor Works**

A unipolar stepper motor typically has four phases and operates on DC power. By correctly timing the electrical current to the motor's phases, you can make the motor rotate step by step. Imagine the motor's center containing a gear-shaped magnet (the rotor) surrounded by several teeth numbered 0 to 5. Around these teeth are eight magnetic poles arranged in pairs (A to D), connected by coils.

.. image:: img/step_interal.png
  :align: center

When you power on different switches connected to these coils (labeled SA, SB, SC, and SD), you control which magnetic poles are activated. For example, if switch SB is on (and the others are off), magnetic poles B align with certain teeth on the rotor, causing it to move. When you turn on switch SC next, the rotor turns to align with magnetic poles C, and so on. By cycling through switches A, B, C, and D, the rotor spins continuously.

**ULN2003 Module**

.. image:: img/step_uln2003.png
    :align: center

The ULN2003 stepper motor driver module is vital for integrating the stepper motor into circuits. It works as a 7-channel inverter, meaning it converts input signals into the needed output actions for the motor. For example, if a high signal is sent to IN1 and low signals to IN2, IN3, and IN4, then OUT1 turns low, and the other outputs stay high, making the motor rotate a step. By providing specific sequences like this, the motor can rotate smoothly step by step. The ULN2003 simplifies controlling the timing sequences necessary for the motor's operation.
