.. note::

    Hello, welcome to the SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasts Community on Facebook! Dive deeper into Raspberry Pi, Arduino, and ESP32 with fellow enthusiasts.

    **Why Join?**

    - **Expert Support**: Solve post-sale issues and technical challenges with help from our community and team.
    - **Learn & Share**: Exchange tips and tutorials to enhance your skills.
    - **Exclusive Previews**: Get early access to new product announcements and sneak peeks.
    - **Special Discounts**: Enjoy exclusive discounts on our newest products.
    - **Festive Promotions and Giveaways**: Take part in giveaways and holiday promotions.

    👉 Ready to explore and create with us? Click [|link_sf_facebook|] and join today!

class ``ADXL345`` - accelemeter
===============================

**Usage**

.. code-block:: python

    from robot_hat import ADXL345

    accel = ADXL345()                     # create an ADXL345 object
    x_val = accel.read(accel.X)           # read an X(0) value
    y_val = accel.read(1)                 # read an Y(1) value
    z_val = accel.read(2)                 # read a Z(2) value

**Constructors**


``class robot_hat.ADXL345(address=0x53)``: Create an ADXL345 object. This
allows you to then read adxl345 accelerator values.

**Methods**


-  ``read`` - Read the value with the axis and return it. The unit is gravity acceleration(about 9.8m/s2).

.. code-block:: python

    ADXL345.read(axis)

**Constants**


-  ``X`` - x axis
-  ``Y`` - y axis
-  ``Z`` - z axis

