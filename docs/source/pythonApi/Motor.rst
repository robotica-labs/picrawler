.. note::

    Hello, welcome to the SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasts Community on Facebook! Dive deeper into Raspberry Pi, Arduino, and ESP32 with fellow enthusiasts.

    **Why Join?**

    - **Expert Support**: Solve post-sale issues and technical challenges with help from our community and team.
    - **Learn & Share**: Exchange tips and tutorials to enhance your skills.
    - **Exclusive Previews**: Get early access to new product announcements and sneak peeks.
    - **Special Discounts**: Enjoy exclusive discounts on our newest products.
    - **Festive Promotions and Giveaways**: Take part in giveaways and holiday promotions.

    👉 Ready to explore and create with us? Click [|link_sf_facebook|] and join today!

.. _class_motor:

class ``Motor`` - motor control
===========================================

**Usage**

.. code-block:: python

    from robot_hat import Motor

    motor = Motor()                     # Create a motor object
    motor = motor.wheel(100)            # Set the motor speed to 100

**Constructors**

``class robot_hat.Motor()``: Create a motor object, you can use it to control the motors.

**Methods**

-  ``wheel`` - Control the speed and direction of the motor.

.. code-block:: python

    # The speed range is -100 to 100, and the positive and negative values represent the direction of rotation of the motor.
    motor.wheel(100)

    # The second parameter, filled with 0 or 1, is used to control a specific motor.
    motor.wheel(100,1)
