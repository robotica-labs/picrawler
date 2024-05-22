.. note::

    Hallo und willkommen in der SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasten-Gemeinschaft auf Facebook! Tauchen Sie tiefer ein in die Welt von Raspberry Pi, Arduino und ESP32 mit anderen Enthusiasten.

    **Warum beitreten?**

    - **Expertenunterstützung**: Lösen Sie Nachverkaufsprobleme und technische Herausforderungen mit Hilfe unserer Gemeinschaft und unseres Teams.
    - **Lernen & Teilen**: Tauschen Sie Tipps und Anleitungen aus, um Ihre Fähigkeiten zu verbessern.
    - **Exklusive Vorschauen**: Erhalten Sie frühzeitigen Zugang zu neuen Produktankündigungen und exklusiven Einblicken.
    - **Spezialrabatte**: Genießen Sie exklusive Rabatte auf unsere neuesten Produkte.
    - **Festliche Aktionen und Gewinnspiele**: Nehmen Sie an Gewinnspielen und Feiertagsaktionen teil.

    👉 Sind Sie bereit, mit uns zu erkunden und zu erschaffen? Klicken Sie auf [|link_sf_facebook|] und treten Sie heute bei!

Klasse ``Music`` - Noten und Schläge
========================================

**Verwendung**

.. code-block:: python

    from robot_hat import Music, Buzzer

    m = Music()           # Ein Musik-Objekt erstellen
    buzzer = Buzzer("P0")
    m.tempo(120)          # Aktuelles Tempo auf 120 Schläge pro Minute setzen

    # Spiele Mittel-C, D, E, F, G, A, B jeweils einen Schlag lang.
    buzzer.play(m.note("Middle C"), m.beat(1))
    buzzer.play(m.note("Middle D"), m.beat(1))
    buzzer.play(m.note("Middle E"), m.beat(1))
    buzzer.play(m.note("Middle F"), m.beat(1))
    buzzer.play(m.note("Middle G"), m.beat(1))
    buzzer.play(m.note("Middle A"), m.beat(1))
    buzzer.play(m.note("Middle B"), m.beat(1))

    song = './music/test.wav'
    
    m.music_set_volume(80)
    print('Musikdauer', m.sound_length(file_name))
    m.sound_play(song)

**Konstruktoren**

``class robot_hat.Music()``: Erstellt ein Music-Objekt, das die Steuerung oder Abfrage von Musik ermöglicht.

**Methoden**

-  ``note`` - Ermittelt die Frequenz der Note. Der Eingabestring muss die Konstante ``NOTE`` sein.

.. code-block:: python

    Music.note("Middle D")
    Music.note("High A#")

-  ``beat`` - Wandelt Schläge in Millisekunden um. Der Eingabewert kann ein Float sein, wie ``0.5`` für einen halben Schlag oder ``0.25`` für einen Viertelschlag.

.. code-block:: python

    Music.beat(0.5)
    Music.beat(0.125)

-  ``tempo`` - Abfrage oder Festlegung des Tempos, der Eingabewert ist in bpm (Schläge pro Minute).

.. code-block:: python

    Music.tempo()
    Music.tempo(120)

-  ``play_tone_for`` - Spielt einen Ton. Die Eingabe sind Note und Schlag, wie ``Music.note("Middle D"), Music.beat(0.5)``.

.. code-block:: python

    Music.play_tone_for(Music.note("Middle D"), Music.beat(0.5))

-  ``sound_play`` - Spielt Musikdateien ab.

.. code-block:: python
    
    sound_play(file_name)

-  ``background_music`` - Hintergrundmusik-Wiedergabe (Dateiname, Anzahl der Schleifen, Startposition der Musikdatei, Lautstärke).

.. code-block:: python

    background_music(file_name, loops=-1, start=0.0, volume=50)

-  ``music_set_volume`` - Lautstärke einstellen
    
.. code-block:: python

    music_set_volume(value=50)

-  ``music_stop`` - stoppen
    
.. code-block:: python

    music_stop()

-  ``music_pause`` - pausieren
    
.. code-block:: python

    music_pause()

-  ``music_unpause`` - fortsetzen
    
.. code-block:: python

    music_unpause()

-  ``sound_length`` - Gibt die Dauer der Musikdatei zurück.
    
.. code-block:: python

    len = sound_length(file_name)

