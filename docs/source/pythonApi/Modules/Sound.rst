.. note::

    Hallo und willkommen in der SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasten-Gemeinschaft auf Facebook! Tauchen Sie tiefer ein in die Welt von Raspberry Pi, Arduino und ESP32 mit anderen Enthusiasten.

    **Warum beitreten?**

    - **Expertenunterstützung**: Lösen Sie Nachverkaufsprobleme und technische Herausforderungen mit Hilfe unserer Gemeinschaft und unseres Teams.
    - **Lernen & Teilen**: Tauschen Sie Tipps und Anleitungen aus, um Ihre Fähigkeiten zu verbessern.
    - **Exklusive Vorschauen**: Erhalten Sie frühzeitigen Zugang zu neuen Produktankündigungen und exklusiven Einblicken.
    - **Spezialrabatte**: Genießen Sie exklusive Rabatte auf unsere neuesten Produkte.
    - **Festliche Aktionen und Gewinnspiele**: Nehmen Sie an Gewinnspielen und Feiertagsaktionen teil.

    👉 Sind Sie bereit, mit uns zu erkunden und zu erschaffen? Klicken Sie auf [|link_sf_facebook|] und treten Sie heute bei!

Klasse ``Sound`` - Schallsensor
===============================

**Verwendung**

.. code-block:: python

    from robot_hat import Sound, ADC

    pin = ADC("A0")
    sound = Sound(pin)                          # Schallsensor-Objekt aus einem Pin erstellen
    val = sound.read_raw()                      # Analogen Wert lesen

    average_val = sound.read_raw(time = 100)    # Durchschnittlichen analogen Wert lesen

**Konstruktoren**

``class robot_hat.Sound(pin)``: Erstellt ein Sound-Objekt, das mit dem gegebenen Pin verknüpft ist. Dadurch können Sie analoge Werte an diesem Pin auslesen.

**Methoden**

-  ``read_raw`` - Liest den Wert am analogen Pin und gibt ihn zurück. Der zurückgegebene Wert liegt zwischen 0 und 4095.

.. code-block:: python

    Sound.read_raw()