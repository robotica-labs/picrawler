.. note::

    Hello, welcome to the SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasts Community on Facebook! Dive deeper into Raspberry Pi, Arduino, and ESP32 with fellow enthusiasts.

    **Why Join?**

    - **Expert Support**: Solve post-sale issues and technical challenges with help from our community and team.
    - **Learn & Share**: Exchange tips and tutorials to enhance your skills.
    - **Exclusive Previews**: Get early access to new product announcements and sneak peeks.
    - **Special Discounts**: Enjoy exclusive discounts on our newest products.
    - **Festive Promotions and Giveaways**: Take part in giveaways and holiday promotions.

    👉 Ready to explore and create with us? Click [|link_sf_facebook|] and join today!

.. _class_adc:

class ``ADC`` - analog to digital converter
===========================================

**Usage**

.. code-block:: python

    from robot_hat import ADC

    adc = ADC("A0")                     # create an analog object from a pin
    val = adc.read()                    # Read values from analog pins

**Constructors**

``class robot_hat.ADC(pin)``: Create an ADC object associated with the given pin. This allows you to then read analog values on that pin.

**Methods**

-  ``read`` - Read the value on the analog pin and return it. The returned value will be between 0 and 4095.

.. code-block:: python

    ADC.read()
