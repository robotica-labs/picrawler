.. note::

    Hello, welcome to the SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasts Community on Facebook! Dive deeper into Raspberry Pi, Arduino, and ESP32 with fellow enthusiasts.

    **Why Join?**

    - **Expert Support**: Solve post-sale issues and technical challenges with help from our community and team.
    - **Learn & Share**: Exchange tips and tutorials to enhance your skills.
    - **Exclusive Previews**: Get early access to new product announcements and sneak peeks.
    - **Special Discounts**: Enjoy exclusive discounts on our newest products.
    - **Festive Promotions and Giveaways**: Take part in giveaways and holiday promotions.

    👉 Ready to explore and create with us? Click [|link_sf_facebook|] and join today!

class ``Sound`` - sound sensor
==============================

**Usage**

.. code-block:: python

    from robot_hat import Sound, ADC

    pin = ADC("A0")
    sound = Sound(pin)                         # create a Sound object from a pin
    val = sound.read_raw()                     # read an analog value

    average_val = sound.read_raw(time = 100)   # read an average analog value

**Constructors**

``class robot_hat.Sound(pin)``: Create a Sound object associated with the given pin. This allows you to read analog values on that pin.

**Methods**

-  ``read_raw`` - Read the value on the analog pin and return it. The returned value will be between 0 and 4095.

.. code-block:: python

    Sound.read_raw()


