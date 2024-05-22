.. note::

    Hallo und willkommen in der SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasten-Gemeinschaft auf Facebook! Tauchen Sie tiefer ein in die Welt von Raspberry Pi, Arduino und ESP32 mit anderen Enthusiasten.

    **Warum beitreten?**

    - **Expertenunterstützung**: Lösen Sie Nachverkaufsprobleme und technische Herausforderungen mit Hilfe unserer Gemeinschaft und unseres Teams.
    - **Lernen & Teilen**: Tauschen Sie Tipps und Anleitungen aus, um Ihre Fähigkeiten zu verbessern.
    - **Exklusive Vorschauen**: Erhalten Sie frühzeitigen Zugang zu neuen Produktankündigungen und exklusiven Einblicken.
    - **Spezialrabatte**: Genießen Sie exklusive Rabatte auf unsere neuesten Produkte.
    - **Festliche Aktionen und Gewinnspiele**: Nehmen Sie an Gewinnspielen und Feiertagsaktionen teil.

    👉 Sind Sie bereit, mit uns zu erkunden und zu erschaffen? Klicken Sie auf [|link_sf_facebook|] und treten Sie heute bei!

Klasse ``TTS`` - Text-zu-Sprache
================================

**Verwendung**

.. code-block:: python

       from robot_hat import *

       tts = TTS()                       # Ein TTS-Objekt erzeugen
       tts.say('hello')                  # Wort ausgeben

       # tts.write('hi')                 # Wort ausgeben
       tts.lang('en-GB')                 # Sprache ändern

       tts.supported_lang()              # Unterstützte Sprachen abfragen

**Konstruktoren**

``class robot_hat.TTS(engine)``: Erzeugt ein TTS-Objekt. Als ``engine`` können ``"espeak"``, ``"gtts"`` für Google TTS oder ``polly`` für AWS Polly verwendet werden.

**Methoden**

-  ``say`` - Wort über TTS ausgeben.

.. code-block:: python

       TTS.say(words)

-  ``lang`` - Sprache in TTS ändern.

.. code-block:: python

       TTS.lang(language)

-  ``supported_lang`` - Alle unterstützten Sprachen abfragen.

.. code-block:: python

       TTS.supported_lang()

-  Parameteranpassung

.. code-block:: python

       # amp: Amplitude, Lautstärke
       # speed: Sprechgeschwindigkeit
       # gap: Pause
       # pitch: Tonhöhe
       def espeak_params(self, amp=None, speed=None, gap=None, pitch=None)







