.. note::

    Hallo und willkommen in der SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasten-Gemeinschaft auf Facebook! Tauchen Sie tiefer ein in die Welt von Raspberry Pi, Arduino und ESP32 mit anderen Enthusiasten.

    **Warum beitreten?**

    - **Expertenunterstützung**: Lösen Sie Nachverkaufsprobleme und technische Herausforderungen mit Hilfe unserer Gemeinschaft und unseres Teams.
    - **Lernen & Teilen**: Tauschen Sie Tipps und Anleitungen aus, um Ihre Fähigkeiten zu verbessern.
    - **Exklusive Vorschauen**: Erhalten Sie frühzeitigen Zugang zu neuen Produktankündigungen und exklusiven Einblicken.
    - **Spezialrabatte**: Genießen Sie exklusive Rabatte auf unsere neuesten Produkte.
    - **Festliche Aktionen und Gewinnspiele**: Nehmen Sie an Gewinnspielen und Feiertagsaktionen teil.

    👉 Sind Sie bereit, mit uns zu erkunden und zu erschaffen? Klicken Sie auf [|link_sf_facebook|] und treten Sie heute bei!

Klasse ``Buzzer`` - passiver Summer
=====================================

**Verwendung**

.. code-block:: python

    from robot_hat import PWM, Buzzer, Music

    pwm = PWM("A0")                          # Ein PWM-Objekt erzeugen
    buzzer = Buzzer(pwm)                     # Ein Buzzer-Objekt mit PWM-Objekt erzeugen
    music = Music()                          # Ein Musik-Objekt erzeugen

    buzzer.play(music.note("Low C"), music.beat(1))  # Tiefe C-Ton für 1 Schlag spielen
    buzzer.play(music.note("Middle C#"))             # Mittlere C# spielen
    buzzer.off()                                     # Summer ausschalten

**Konstruktoren**

``class robot_hat.Buzzer(pwm)``: Ein Buzzer-Objekt erzeugen, das mit dem gegebenen PWM-Objekt assoziiert ist. Dies ermöglicht die Steuerung des Buzzers.

**Methoden**

-  ``on`` - Schaltet den Buzzer mit einer Rechteckwelle ein.

.. code-block:: python

    Buzzer.on()

-  ``off`` - Schaltet den Buzzer aus.

.. code-block:: python

    Buzzer.off()

-  ``freq`` - Legt die Frequenz der Rechteckwelle fest.

.. code-block:: python

    Buzzer.freq(frequency)

-  ``play`` - Lässt den Buzzer mit einer bestimmten Frequenz erklingen und stoppt nach einer bestimmten Verzögerungszeit in Millisekunden.

.. code-block:: python

    Buzzer.play(freq, ms)
    Buzzer.play(freq)

