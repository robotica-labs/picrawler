.. note::

    Hello, welcome to the SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasts Community on Facebook! Dive deeper into Raspberry Pi, Arduino, and ESP32 with fellow enthusiasts.

    **Why Join?**

    - **Expert Support**: Solve post-sale issues and technical challenges with help from our community and team.
    - **Learn & Share**: Exchange tips and tutorials to enhance your skills.
    - **Exclusive Previews**: Get early access to new product announcements and sneak peeks.
    - **Special Discounts**: Enjoy exclusive discounts on our newest products.
    - **Festive Promotions and Giveaways**: Take part in giveaways and holiday promotions.

    👉 Ready to explore and create with us? Click [|link_sf_facebook|] and join today!

class ``Servo`` - 3-wire pwm servo driver
=========================================

**Usage**

.. code-block:: python

    from robot_hat import Servo, PWM

    pin = PWM("P0")
    ser = Servo(pin)                      # create a Servo object
    val = ser.angle(60)                   # set the servo angle

**Constructors**

``class robot_hat.Servo(pin)``: Create a Servo object associated with the given pin. This allows you to set the angle values.

**Methods**

-  ``angle`` - set the angle values between -90 and 90.

.. code-block:: python

    Servo.angle(90)


