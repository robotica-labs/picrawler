.. note::

    Hallo und willkommen in der SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasten-Gemeinschaft auf Facebook! Tauchen Sie tiefer ein in die Welt von Raspberry Pi, Arduino und ESP32 mit anderen Enthusiasten.

    **Warum beitreten?**

    - **Expertenunterstützung**: Lösen Sie Nachverkaufsprobleme und technische Herausforderungen mit Hilfe unserer Gemeinschaft und unseres Teams.
    - **Lernen & Teilen**: Tauschen Sie Tipps und Anleitungen aus, um Ihre Fähigkeiten zu verbessern.
    - **Exklusive Vorschauen**: Erhalten Sie frühzeitigen Zugang zu neuen Produktankündigungen und exklusiven Einblicken.
    - **Spezialrabatte**: Genießen Sie exklusive Rabatte auf unsere neuesten Produkte.
    - **Festliche Aktionen und Gewinnspiele**: Nehmen Sie an Gewinnspielen und Feiertagsaktionen teil.

    👉 Sind Sie bereit, mit uns zu erkunden und zu erschaffen? Klicken Sie auf [|link_sf_facebook|] und treten Sie heute bei!

Klasse ``Servo`` - 3-Draht-PWM-Servotreiber
==============================================

**Verwendung**

.. code-block:: python

    from robot_hat import Servo, PWM

    pin = PWM("P0")
    ser = Servo(pin)                      # Ein Servo-Objekt erzeugen
    val = ser.angle(60)                   # Servowinkel einstellen

**Konstruktoren**

``class robot_hat.Servo(pin)``: Erzeugt ein Servo-Objekt, das mit dem angegebenen Pin assoziiert ist. Dadurch können Winkelwerte eingestellt werden.

**Methoden**

-  ``angle`` - Stellt die Winkelwerte zwischen -90 und 90 ein.

.. code-block:: python

    Servo.angle(90)