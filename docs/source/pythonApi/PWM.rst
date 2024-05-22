.. note::

    Hello, welcome to the SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasts Community on Facebook! Dive deeper into Raspberry Pi, Arduino, and ESP32 with fellow enthusiasts.

    **Why Join?**

    - **Expert Support**: Solve post-sale issues and technical challenges with help from our community and team.
    - **Learn & Share**: Exchange tips and tutorials to enhance your skills.
    - **Exclusive Previews**: Get early access to new product announcements and sneak peeks.
    - **Special Discounts**: Enjoy exclusive discounts on our newest products.
    - **Festive Promotions and Giveaways**: Take part in giveaways and holiday promotions.

    👉 Ready to explore and create with us? Click [|link_sf_facebook|] and join today!

.. _class_pwm:

class ``PWM`` - pulse width modulation
======================================

**Usage**

.. code-block:: python

    from robot_hat import PWM

    pwm = PWM('P0')                                 # create a PWM object from a pin
    PWM.freq(*freq)                                 #Frequency (0-65535, unit Hz)
    PWM.prescaler(*prescaler)                       #Prescaler
    PWM.period(*arr)  
    PWM.pulse_width(*pulse_width)                   # Pulse width (pulse_width < period)
    PWM.pulse_width_percent(*pulse_width_percent)   # Duty cycle (0-100)

**Constructors**

``class robot_hat.PWM(channel)``: Create a PWM object associated with the given pin. This allows you set up the pwm function on that pin.

**Methods**

-  ``freq`` - Set the frequency of the pwm channel.

.. code-block:: python

    PWM.freq(50)

-  ``prescaler`` - Set the prescaler for the pwm channel.

.. code-block:: python

    PWM.prescaler(50)

-  ``period`` - Set the period of the pwm channel.

.. code-block:: python

    PWM.period(100)

-  ``pulse_width`` - Set the pulse width of the pwm channel.

.. code-block:: python

    PWM.pulse_width(10)

-  ``pulse_width_percent`` - Sets the pulse width percentage of the pwm channel.

.. code-block:: python

    PWM.pulse_width_percent(50)


