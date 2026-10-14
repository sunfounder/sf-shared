.. note::

    Hello, welcome to the SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasts Community on Facebook! Dive deeper into Raspberry Pi, Arduino, and ESP32 with fellow enthusiasts.

    **Why Join?**

    - **Expert Support**: Solve post-sale issues and technical challenges with help from our community and team.
    - **Learn & Share**: Exchange tips and tutorials to enhance your skills.
    - **Exclusive Previews**: Get early access to new product announcements and sneak peeks.
    - **Special Discounts**: Enjoy exclusive discounts on our newest products.
    - **Festive Promotions and Giveaways**: Take part in giveaways and holiday promotions.

    👉 Ready to explore and create with us? Click [|link_sf_facebook|] and join today!

.. _cpn_motor_clamp:

Motor Ferrite Clamp
========================

.. image:: img/motor_clamp.png
    :width: 70%
    :align: center

The black oval on the motor cable is a **ferrite clamp** — two halves of a nickel-zinc (NiZn) ferrite pressed around the wire and held shut by the plastic latch you can see on top. It ships fitted to the ``DC Motor XH2.54 <cpn_motor_xh254>``, and it is part of the motor, not packaging.

**Specifications**

* **Type**: Nickel-zinc (NiZn) ferrite bead
* **Model**: UF35A
* **Bore**: 3.5 mm
* **Fits**: the 24 AWG motor cable
* **Position**: about 40 mm from the motor body

**What It Is For**

A brushed motor makes and breaks contact many times per revolution, and every one of those sparks radiates high-frequency noise. That noise travels back down the power wires and can reach the rest of the board — the classic symptoms are a sensor that jumps, a servo that twitches, or an ADC reading that wanders whenever the motor runs.

The ferrite absorbs those high-frequency currents and turns them into a little heat, so much less of the noise leaves the cable. The effect is strongest for the frequencies the motor generates and negligible for the DC the motor uses, which is why the cable can pass through it untouched.

The clamp works in either direction and has no polarity: do not remove it, and if you ever have to refit it, close the latch firmly so both halves touch.

**How It Is Fitted**

The two halves are hinged along one edge and snapped together along the other. Squeeze the latch tabs to open it, lay the cable in the groove, close it, and press until it clicks. The closer it sits to the motor, the shorter the length of cable that can act as an antenna, so keep it near the body rather than at the plug end.
