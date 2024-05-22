.. note::

    Hello, welcome to the SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasts Community on Facebook! Dive deeper into Raspberry Pi, Arduino, and ESP32 with fellow enthusiasts.

    **Why Join?**

    - **Expert Support**: Solve post-sale issues and technical challenges with help from our community and team.
    - **Learn & Share**: Exchange tips and tutorials to enhance your skills.
    - **Exclusive Previews**: Get early access to new product announcements and sneak peeks.
    - **Special Discounts**: Enjoy exclusive discounts on our newest products.
    - **Festive Promotions and Giveaways**: Take part in giveaways and holiday promotions.

    👉 Ready to explore and create with us? Click [|link_sf_facebook|] and join today!

class ``Ultrasonic`` - ultrasonic ranging sensor
================================================

**Usage**

.. code-block:: python

    from robot_hat import Ultrasonic, Pin

    trig = Pin("D0")
    echo = Pin("D1")

    ultrasonic = Ultrasonic(trig, echo)             # create an Ultrasonic object
    val = ultrasonic.read()                         # read an analog value

**Constructors**

``class robot_hat.Ultrasonic(trig, echo)``: Create a Ultrasonic object associated with the given pin. This allows you to then read distance value.

**Methods**

-  ``read`` - Read distance values.

   .. code-block:: python

       Ultrasonic.read(trig, echo)


