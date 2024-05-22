.. note::

    Hallo und willkommen in der SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasten-Gemeinschaft auf Facebook! Tauchen Sie tiefer ein in die Welt von Raspberry Pi, Arduino und ESP32 mit anderen Enthusiasten.

    **Warum beitreten?**

    - **Expertenunterstützung**: Lösen Sie Nachverkaufsprobleme und technische Herausforderungen mit Hilfe unserer Gemeinschaft und unseres Teams.
    - **Lernen & Teilen**: Tauschen Sie Tipps und Anleitungen aus, um Ihre Fähigkeiten zu verbessern.
    - **Exklusive Vorschauen**: Erhalten Sie frühzeitigen Zugang zu neuen Produktankündigungen und exklusiven Einblicken.
    - **Spezialrabatte**: Genießen Sie exklusive Rabatte auf unsere neuesten Produkte.
    - **Festliche Aktionen und Gewinnspiele**: Nehmen Sie an Gewinnspielen und Feiertagsaktionen teil.

    👉 Sind Sie bereit, mit uns zu erkunden und zu erschaffen? Klicken Sie auf [|link_sf_facebook|] und treten Sie heute bei!

.. _class_motor:

Klasse ``Motor`` - Motorsteuerung
=================================

**Verwendung**

.. code-block:: python

    from robot_hat import Motor

    motor = Motor()                      # Ein Motor-Objekt erzeugen
    motor = motor.wheel(100)             # Motorgeschwindigkeit auf 100 setzen

**Konstruktoren**

``class robot_hat.Motor()``: Erzeugt ein Motor-Objekt zur Steuerung der Motoren.

**Methoden**

-  ``wheel`` - Steuert Geschwindigkeit und Richtung des Motors.

.. code-block:: python

    # Der Geschwindigkeitsbereich liegt zwischen -100 und 100, wobei positive und negative Werte die Drehrichtung des Motors angeben.
    motor.wheel(100)

    # Der zweite Parameter, gefüllt mit 0 oder 1, dient zur Steuerung eines spezifischen Motors.
    motor.wheel(100, 1)