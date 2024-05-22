.. note::

    Hello, welcome to the SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasts Community on Facebook! Dive deeper into Raspberry Pi, Arduino, and ESP32 with fellow enthusiasts.

    **Why Join?**

    - **Expert Support**: Solve post-sale issues and technical challenges with help from our community and team.
    - **Learn & Share**: Exchange tips and tutorials to enhance your skills.
    - **Exclusive Previews**: Get early access to new product announcements and sneak peeks.
    - **Special Discounts**: Enjoy exclusive discounts on our newest products.
    - **Festive Promotions and Giveaways**: Take part in giveaways and holiday promotions.

    👉 Ready to explore and create with us? Click [|link_sf_facebook|] and join today!

class ``Joystick`` - 3-axis joystick
====================================

**Usage**

.. code-block:: python

    from robot_hat import Joystick, ADC, Pin

    x_pin = ADC("A0")
    y_pin = ADC("A1")
    btn_pin = Pin("D1")

    joystick = Joystick(x_pin, y_pin, btn_pin)         # create a Joystick object
    val = joystick.read(0)                             # read an axis value
    status = joystick.read_status()                    # read the status of joystick

**Constructors**


``class robot_hat.Joystick(pin)``: Create a Joystick object associated with the given pin. This allows you to read values from Joystick.

**Methods**


-  ``read`` - Read the value on the given pins and return them.

.. code-block:: python

    Joystick.read(Xpin, Ypin, Btpin)

-  ``read_status`` - read the status of joystick.

.. code-block:: python

    Joystick.read_status()


