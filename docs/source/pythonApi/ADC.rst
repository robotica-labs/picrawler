.. note::

    Hallo und willkommen in der SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasten-Gemeinschaft auf Facebook! Tauchen Sie tiefer ein in die Welt von Raspberry Pi, Arduino und ESP32 mit anderen Enthusiasten.

    **Warum beitreten?**

    - **Expertenunterstützung**: Lösen Sie Nachverkaufsprobleme und technische Herausforderungen mit Hilfe unserer Gemeinschaft und unseres Teams.
    - **Lernen & Teilen**: Tauschen Sie Tipps und Anleitungen aus, um Ihre Fähigkeiten zu verbessern.
    - **Exklusive Vorschauen**: Erhalten Sie frühzeitigen Zugang zu neuen Produktankündigungen und exklusiven Einblicken.
    - **Spezialrabatte**: Genießen Sie exklusive Rabatte auf unsere neuesten Produkte.
    - **Festliche Aktionen und Gewinnspiele**: Nehmen Sie an Gewinnspielen und Feiertagsaktionen teil.

    👉 Sind Sie bereit, mit uns zu erkunden und zu erschaffen? Klicken Sie auf [|link_sf_facebook|] und treten Sie heute bei!

.. _class_adc:

Klasse ``ADC`` - Analog-Digital-Wandler
========================================

**Verwendung**

.. code-block:: python

    from robot_hat import ADC

    adc = ADC("A0")                    # Erzeugt ein Analogobjekt von einem Pin
    val = adc.read()                   # Liest Werte von analogen Pins

**Konstruktoren**

``class robot_hat.ADC(pin)``: Erstellt ein ADC-Objekt, das mit dem angegebenen Pin verknüpft ist. Dies ermöglicht Ihnen, analoge Werte an diesem Pin auszulesen.

**Methoden**

-  ``read`` - Liest den Wert am analogen Pin und gibt ihn zurück. Der zurückgegebene Wert liegt zwischen 0 und 4095.

.. code-block:: python

    ADC.read()


