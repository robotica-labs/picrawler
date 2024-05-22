.. note::

    Hallo und willkommen in der SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasten-Gemeinschaft auf Facebook! Tauchen Sie tiefer ein in die Welt von Raspberry Pi, Arduino und ESP32 mit anderen Enthusiasten.

    **Warum beitreten?**

    - **Expertenunterstützung**: Lösen Sie Nachverkaufsprobleme und technische Herausforderungen mit Hilfe unserer Gemeinschaft und unseres Teams.
    - **Lernen & Teilen**: Tauschen Sie Tipps und Anleitungen aus, um Ihre Fähigkeiten zu verbessern.
    - **Exklusive Vorschauen**: Erhalten Sie frühzeitigen Zugang zu neuen Produktankündigungen und exklusiven Einblicken.
    - **Spezialrabatte**: Genießen Sie exklusive Rabatte auf unsere neuesten Produkte.
    - **Festliche Aktionen und Gewinnspiele**: Nehmen Sie an Gewinnspielen und Feiertagsaktionen teil.

    👉 Sind Sie bereit, mit uns zu erkunden und zu erschaffen? Klicken Sie auf [|link_sf_facebook|] und treten Sie heute bei!

Klasse ``ADXL345`` - Beschleunigungsmesser
=============================================

**Verwendung**

.. code-block:: python

    from robot_hat import ADXL345

    accel = ADXL345()                        # Ein ADXL345-Objekt erzeugen
    x_val = accel.read(accel.X)              # Einen X-Wert auslesen
    y_val = accel.read(1)                    # Einen Y-Wert auslesen
    z_val = accel.read(2)                    # Einen Z-Wert auslesen

**Konstruktoren**

``class robot_hat.ADXL345(address=0x53)``: Ein ADXL345-Objekt erzeugen. Damit können anschließend Beschleunigungswerte ausgelesen werden.

**Methoden**

-  ``read`` - Liest den Wert der jeweiligen Achse und gibt ihn zurück. Die Einheit ist die Erdbeschleunigung (etwa 9,8 m/s²).

.. code-block:: python

    ADXL345.read(axis)

**Konstanten**

-  ``X`` - X-Achse
-  ``Y`` - Y-Achse
-  ``Z`` - Z-Achse



