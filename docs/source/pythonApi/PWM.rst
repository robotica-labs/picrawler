.. note::

    Hallo und willkommen in der SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasten-Gemeinschaft auf Facebook! Tauchen Sie tiefer ein in die Welt von Raspberry Pi, Arduino und ESP32 mit anderen Enthusiasten.

    **Warum beitreten?**

    - **Expertenunterstützung**: Lösen Sie Nachverkaufsprobleme und technische Herausforderungen mit Hilfe unserer Gemeinschaft und unseres Teams.
    - **Lernen & Teilen**: Tauschen Sie Tipps und Anleitungen aus, um Ihre Fähigkeiten zu verbessern.
    - **Exklusive Vorschauen**: Erhalten Sie frühzeitigen Zugang zu neuen Produktankündigungen und exklusiven Einblicken.
    - **Spezialrabatte**: Genießen Sie exklusive Rabatte auf unsere neuesten Produkte.
    - **Festliche Aktionen und Gewinnspiele**: Nehmen Sie an Gewinnspielen und Feiertagsaktionen teil.

    👉 Sind Sie bereit, mit uns zu erkunden und zu erschaffen? Klicken Sie auf [|link_sf_facebook|] und treten Sie heute bei!

.. _class_pwm:

Klasse ``PWM`` - Pulsweitenmodulation
=======================================

**Verwendung**

.. code-block:: python

    from robot_hat import PWM

    pwm = PWM('P0')                              # Erzeugt ein PWM-Objekt von einem Pin
    PWM.freq(*freq)                              # Frequenz (0-65535, Einheit Hz)
    PWM.prescaler(*prescaler)                    # Vorteiler
    PWM.period(*arr)  
    PWM.pulse_width(*pulse_width)                # Pulsbreite (pulse_width < period)
    PWM.pulse_width_percent(*pulse_width_percent)# Tastverhältnis (0-100)

**Konstruktoren**

``class robot_hat.PWM(channel)``: Erstellt ein PWM-Objekt, das mit dem angegebenen Pin verknüpft ist. Dies ermöglicht Ihnen, die PWM-Funktion an diesem Pin einzurichten.

**Methoden**

-  ``freq`` - Legt die Frequenz des PWM-Kanals fest.

.. code-block:: python

    PWM.freq(50)

-  ``prescaler`` - Legt den Vorteiler für den PWM-Kanal fest.

.. code-block:: python

    PWM.prescaler(50)

-  ``period`` - Legt die Periode des PWM-Kanals fest.

.. code-block:: python

    PWM.period(100)

-  ``pulse_width`` - Legt die Pulsbreite des PWM-Kanals fest.

.. code-block:: python

    PWM.pulse_width(10)

-  ``pulse_width_percent`` - Legt die Pulsbreitenprozentsatz des PWM-Kanals fest.

.. code-block:: python

    PWM.pulse_width_percent(50)
