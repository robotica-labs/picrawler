.. note::

    Hello, welcome to the SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasts Community on Facebook! Dive deeper into Raspberry Pi, Arduino, and ESP32 with fellow enthusiasts.

    **Why Join?**

    - **Expert Support**: Solve post-sale issues and technical challenges with help from our community and team.
    - **Learn & Share**: Exchange tips and tutorials to enhance your skills.
    - **Exclusive Previews**: Get early access to new product announcements and sneak peeks.
    - **Special Discounts**: Enjoy exclusive discounts on our newest products.
    - **Festive Promotions and Giveaways**: Take part in giveaways and holiday promotions.

    👉 Ready to explore and create with us? Click [|link_sf_facebook|] and join today!

class ``TTS`` - text to speech
==============================

**Usage**

.. code-block:: python

       from robot_hat import *

       tts = TTS()                     # create a TTS object
       tts.say('hello')                # write word

       # tts.write('hi')                # write word
       tts.lang('en-GB')                # change language

       tts.supported_lang()            # return language

**Constructors**


``class robot_hat.TTS(engine)``: Create a TTS object, ``engine`` could be ``"espeak"`` as Espeak, ``"gtts"`` as Google TTS and ``polly`` as AWS Polly.

**Methods**


- ``say`` - Write word on TTS.

.. code-block:: python

       TTS.say(words)

-  ``lang`` - Change on TTS.

.. code-block:: python

       TTS.lang(language)

-  ``supported_lang`` - Inquire all supported language.

.. code-block:: python

       TTS.supported_lang()

-  parameter adjustment

.. code-block:: python

       # amp: amplitude, volume
       # speed: speaking speed
       # gap: gap
       # pitch: pitch
       def espeak_params(self, amp=None, speed=None, gap=None, pitch=None)

