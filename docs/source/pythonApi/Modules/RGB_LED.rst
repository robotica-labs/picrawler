.. note::

    Hello, welcome to the SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasts Community on Facebook! Dive deeper into Raspberry Pi, Arduino, and ESP32 with fellow enthusiasts.

    **Why Join?**

    - **Expert Support**: Solve post-sale issues and technical challenges with help from our community and team.
    - **Learn & Share**: Exchange tips and tutorials to enhance your skills.
    - **Exclusive Previews**: Get early access to new product announcements and sneak peeks.
    - **Special Discounts**: Enjoy exclusive discounts on our newest products.
    - **Festive Promotions and Giveaways**: Take part in giveaways and holiday promotions.

    👉 Ready to explore and create with us? Click [|link_sf_facebook|] and join today!

class ``RGB_LED`` - rgb LED
===========================

**Usage**

.. code-block:: python

    from robot_hat import PWM, RGB_LED

    r = PWM("P0")
    g = PWM("P1")
    b = PWM("P2")

    rgb = RGB_LED(r, g, b)                       # Create a RGB_LED object
    val = rgb.write('#FFFFFF')                   # Write in the color in hexadecimal.

**Constructors**

``class robot_hat.RGB_LED(Rpin, Gpin, Bpin)``: Create a ``RGB_LED`` object associated with the given pin. This allows you set the color of RGB LED. 
Input ``Rpin``, ``Gpin``, ``Bpin`` must be ``PWM`` object from ``robot_hat.PWM``.

**Methods**


-  ``write`` - Writing a specific color to the RGB LED, the color value is represented by hexadecimal for red, green and blue (RGB). Each color has a minimum value of 0 (00 in hexadecimal) and a maximum value of 255 (FF in hexadecimal). Hexadecimal values are written with a # sign followed by three or six hexadecimal characters.

.. code-block:: python

    RGB_LED.write(color)


