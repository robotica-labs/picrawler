.. note::

    Hallo und willkommen in der SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasten-Gemeinschaft auf Facebook! Tauchen Sie tiefer ein in die Welt von Raspberry Pi, Arduino und ESP32 mit anderen Enthusiasten.

    **Warum beitreten?**

    - **Expertenunterstützung**: Lösen Sie Nachverkaufsprobleme und technische Herausforderungen mit Hilfe unserer Gemeinschaft und unseres Teams.
    - **Lernen & Teilen**: Tauschen Sie Tipps und Anleitungen aus, um Ihre Fähigkeiten zu verbessern.
    - **Exklusive Vorschauen**: Erhalten Sie frühzeitigen Zugang zu neuen Produktankündigungen und exklusiven Einblicken.
    - **Spezialrabatte**: Genießen Sie exklusive Rabatte auf unsere neuesten Produkte.
    - **Festliche Aktionen und Gewinnspiele**: Nehmen Sie an Gewinnspielen und Feiertagsaktionen teil.

    👉 Sind Sie bereit, mit uns zu erkunden und zu erschaffen? Klicken Sie auf [|link_sf_facebook|] und treten Sie heute bei!

Klasse ``Joystick`` - 3-Achsen-Joystick
=======================================

**Verwendung**

.. code-block:: python

    from robot_hat import Joystick, ADC, Pin

    x_pin = ADC("A0")
    y_pin = ADC("A1")
    btn_pin = Pin("D1")

    joystick = Joystick(x_pin, y_pin, btn_pin)  # Joystick-Objekt erstellen
    val = joystick.read(0)                      # Achsenwert auslesen
    status = joystick.read_status()             # Joystick-Status auslesen

**Konstruktoren**

``class robot_hat.Joystick(pin)``: Erstellt ein Joystick-Objekt, das mit den angegebenen Pins verknüpft ist. Dies ermöglicht das Auslesen von Werten vom Joystick.

**Methoden**

-  ``read`` - Liest die Werte an den angegebenen Pins und gibt sie zurück.

.. code-block:: python

    Joystick.read(Xpin, Ypin, Btpin)

-  ``read_status`` - Liest den Status des Joysticks.

.. code-block:: python

    Joystick.read_status()

