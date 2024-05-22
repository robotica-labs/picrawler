.. note::

    Hello, welcome to the SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasts Community on Facebook! Dive deeper into Raspberry Pi, Arduino, and ESP32 with fellow enthusiasts.

    **Why Join?**

    - **Expert Support**: Solve post-sale issues and technical challenges with help from our community and team.
    - **Learn & Share**: Exchange tips and tutorials to enhance your skills.
    - **Exclusive Previews**: Get early access to new product announcements and sneak peeks.
    - **Special Discounts**: Enjoy exclusive discounts on our newest products.
    - **Festive Promotions and Giveaways**: Take part in giveaways and holiday promotions.

    👉 Ready to explore and create with us? Click [|link_sf_facebook|] and join today!

.. _class_pin:


class ``Pin`` - control I/O pins
================================

**Usage**

.. code-block:: python

    from robot_hat import Pin

    pin = Pin("D0")                      # create a Pin object from a digital pin
    val = pin.value()                    # read the value on the digital pin

    pin.value(0)                         # set the digital pin to low level

**Constructors**

``class robot_hat.Pin(value)`` : The ``Pin()`` is the basic object to control I/O pins. It has methods to set the pin mode (input, output, etc.) and methods to get or set the level of a digital pin.


**Methods**

-  ``value`` - Read or set the value on the digital pin, the value is 0/1.

.. code-block:: python

    Pin.value() # Without parameters, read gpio level, high level returns 1, low level returns 0.

    Pin.value(0)  # set to low level    
    Pin.value(1)  # set to high level

-  Set the value to the digital pin, same as ``value``.

.. code-block:: python

    Pin.on() # set to high level
    #off() # set to low level
    #high() # set to high level
    #low() # set to low level

-  ``mode`` - Set the mode of GPIO to ``IN`` or ``OUT``.

.. code-block:: python
    
    Pin.mode(GPIO.IN)  # set gipo to INPUT mode

**Availble Pins**

-  ``"D0"``: The Digital pin 0.
-  ``"D1"``: The Digital pin 1.
-  ``"D2"``: The Digital pin 2.
-  ``"D3"``: The Digital pin 3.
-  ``"D4"``: The left motor pin.
-  ``"D5"``: The right motor pin.
-  ``"D6"``
-  ``"D7"``
-  ``"D8"``
-  ``"D9"``
-  ``"SW"``: The USR button.
-  ``"LED"``: The LED on the board.

