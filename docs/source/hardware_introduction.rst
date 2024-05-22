.. note::

    Hallo und willkommen in der SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasten-Gemeinschaft auf Facebook! Tauchen Sie tiefer ein in die Welt von Raspberry Pi, Arduino und ESP32 mit anderen Enthusiasten.

    **Warum beitreten?**

    - **Expertenunterstützung**: Lösen Sie Nachverkaufsprobleme und technische Herausforderungen mit Hilfe unserer Gemeinschaft und unseres Teams.
    - **Lernen & Teilen**: Tauschen Sie Tipps und Anleitungen aus, um Ihre Fähigkeiten zu verbessern.
    - **Exklusive Vorschauen**: Erhalten Sie frühzeitigen Zugang zu neuen Produktankündigungen und exklusiven Einblicken.
    - **Spezialrabatte**: Genießen Sie exklusive Rabatte auf unsere neuesten Produkte.
    - **Festliche Aktionen und Gewinnspiele**: Nehmen Sie an Gewinnspielen und Feiertagsaktionen teil.

    👉 Sind Sie bereit, mit uns zu erkunden und zu erschaffen? Klicken Sie auf [|link_sf_facebook|] und treten Sie heute bei!

Hardware-Einführung
=========================

.. .. image:: img/picar_x_pic7.png

.. **Motoranschluss**
..     * 2-Kanal XH2.54 Motoranschlüsse.
..     * Der Motoranschluss 1 ist mit GPIO 23 und der Motoranschluss 2 mit GPIO 24 verbunden.
..     * API: :ref:`class_motor`, ``0`` für den linken Motoranschluss, ``1`` für den rechten Motoranschluss.

.. **I2C-Anschluss**
..     * 2-Kanal I2C-Anschlüsse vom Raspberry Pi.
..     * API: :ref:`class_i2c`

.. **PWM-Anschluss**
..     * 12-Kanal PWM-Anschlüsse, P0-P12.
..     * API: :ref:`class_pwm`

.. **ADC-Anschluss**
..     * 4-Kanal ADC-Anschlüsse, A0-A3.
..     * API: :ref:`class_adc`

.. **Digitaler Anschluss**
..     * 4-Kanal digitale Anschlüsse, D0-D3.
..     * API: :ref:`class_pin`

.. **Batterieanzeige**
..     * Zwei LEDs leuchten auf, wenn die Spannung höher als 7,8V ist.
..     * Eine LED leuchtet im Bereich von 6,7V bis 7,8V. 
..     * Unter 6,7V sind beide LEDs aus.

.. **LED**
..     * Steuerbar durch Ihr Programm. (Ausgabe von 1 schaltet die LED ein; Ausgabe von 0 schaltet sie aus.)
..     * API: :ref:`class_pin`, Sie können es mit ``Pin("LED")`` definieren.

.. **RST-Taste**
..     * Ein kurzer Druck auf die RST-Taste führt zum Neustart des Programms.
..     * Ein langer Druck auf die RST-Taste, bis die LED aufleuchtet, löst die Bluetooth-Verbindung.

.. **USR-Taste**
..     * Die Funktion der USR-Taste kann durch Ihre Programmierung festgelegt werden. (Drücken führt zu einer Eingabe von "0"; Loslassen zu einer Eingabe von "1".)
..     * API: :ref:`class_pin`, Sie können es mit ``Pin("SW")`` definieren.

.. **Stromschalter**
..     * Schaltet die Stromversorgung des Robot HAT ein/aus.
..     * Nach dem Anschluss an die Stromversorgung startet der Raspberry Pi. Der Robot HAT muss jedoch eingeschaltet werden.

.. **Stromanschluss**
..     * 7-12V PH2.0 2-Pin-Stromversorgung.
..     * Versorgt sowohl den Raspberry Pi als auch den Robot HAT mit Strom.

.. **Bluetooth-Modul**
..     * Da der Raspberry Pi standardmäßig im Slave-Modus Bluetooth unterstützt, können beim Koppeln mit Mobiltelefonen Probleme auftreten. Um die Verbindung zum Ezblock Studio zu erleichtern, haben wir ein separates Bluetooth-Modul hinzugefügt.
..     * Ezblock Studio ist eine von SunFounder entwickelte, individuelle grafische Programmierungsanwendung für den Raspberry Pi. Für weitere Informationen verweisen wir auf: `Ezblock Studio 3 <https://docs.sunfounder.com/projects/ezblock3/en/latest/>`_.

.. **Bluetooth-Anzeige**
..     * Die Bluetooth-Anzeige bleibt bei einer stabilen Bluetooth-Verbindung an, blinkt bei einer Trennung und blinkt schnell bei einer Signalübertragung.

Der Robot Hat V4 bietet 2 Lithium-Batterieladungen, eine 5V/3A DC-DC Entladung, einen I2S-Audioausgang und Lautsprecher, eine einfache Batterieanzeige, mikrocontrollergestützte PWM- und ADC-Treiber sowie Motortreiber.

Eigenschaften:
    * Ruhestrom: < 0.5mA
    * Stromversorgung: USB Typ-C, 5V/2A
    * Ladeleistung: 5V/2A 10W
    * Ausgangsleistung: 5V/3A
    * Mitgelieferte Batterien: 2 x 3,7V 18650 Lithium-Ionen-Batterien, XH2.0 3P Schnittstelle
    * Batterieschutz: Verpolungsschutz
    * Ladeschutz: Unterspannungsschutz, Überspannungsschutz, Ladeausgleich, Überhitzungsschutz
    * Integrierte Ladeanzeige: CHG
    * Integrierte Stromversorgungsanzeige: PWR
    * 2 Batterieanzeige-LEDs an Bord
    * Benutzer-LED und 2 taktile Schalter an Bord
    * Motortreiber: 5V/1.8A x 2
    * 4-Kanal 12-Bit ADC
    * 12-Kanal PWM
    * 4-Kanal digitale Signale
    * Integrierte SPI-Schnittstelle, UART-Schnittstelle, I2C-Schnittstelle
    * Monolautsprecher: 8Ω1W

.. list-table:: Elektrische Eigenschaften
   :widths: 50 25 25 25 25
   :header-rows: 1

   * - Parameter:
     - Minimalwert:
     - Standardwert:
     - Maximalwert:
     - Einheit:
   * - Eingangsspannung:
     - 4.25
     - 5
     - 8.4
     - V
   * - Batterieeingangsspannung:
     - 6.0
     - 7.4
     - 8.4
     - V
   * - Überladeschutz (Batterie):
     -
     - 8.3
     -
     - V
   * - Unterspannungsschutz:
     - 4.15
     - 4.25
     - 4.35
     - V
   * - Überspannungsschutz:
     - 8.3
     - 8.4
     - 8.5
     - V
   * - Ladestrom (5V):
     -
     -
     - 2.0
     - A
   * - Ausgangsstrom (5V):
     -
     -
     - 3.0
     - A
   * - Ausgangsspannung:
     - 5.166
     - 5.246
     - 5.327
     - V
   * - Überhitzungsschutz beim Laden:
     - 125
     - 135
     - 145
     - °C
   * - DC-DC-Überhitzungsschutz:
     - 70
     - 75
     - 80
     - °C
   * - Motor-Ausgangsstrom:
     -
     -
     - 1.8
     - A

Einzelheiten
----------------

**Pin & GPIO**

.. list-table:: Raspberry Pi IO
    :widths: 50 50 50 50
    :header-rows: 1

    * - Robot Hat V4
      - Raspberry Pi
      - Robot Hat V4
      - Raspberry Pi
    * - NC
      - 3V3
      - 5V
      - 5V
    * - SDA
      - SDA
      - 5V
      - 5V
    * - SCL
      - SCL
      - GND
      - GND
    * - D1
      - GPIO4
      - TXD
      - TXD
    * - GND
      - GND
      - RXD
      - RXD
    * - D0
      - GPIO17
      - I2S BCLK
      - GPIO18
    * - D2
      - GPIO27
      - GND
      - GND
    * - D3
      - GPIO22
      - MOTOR 1 RICHTUNG
      - GPIO23
    * - NC
      - 3V3
      - MOTOR 2 RICHTUNG
      - GPIO24
    * - SPI MOSI
      - MOSI
      - GND
      - GND
    * - SPI MISO
      - MISO
      - USR TASTE     
      - GPIO25
    * - SPI SCLK
      - SCLK
      - SPI CE0
      - CE0
    * - GND
      - GND
      - NC
      - CE1
    * - NC
      - ID_SD
      - NC
      - ID_SC
    * - MCU Reset
      - GPIO5
      - GND
      - GND
    * - (SPI)BSY
      - GPIO6
      - Board-Kennung 2
      - GPIO12
    * - Board-Kennung 1
      - GPIO13
      - GND
      - GND
    * - I2S LRCLK
      - GPIO19
      - RST TASTE
      - GPIO16
    * - BENUTZER LED
      - GPIO26
      - NC
      - GPIO20
    * - GND
      - GND
      - I2S SDATA
      - GPIO21



**Digital IO**

Das Robot HAT verfügt über 4 Sets von 3-Pin-Digitalpins im P2.54-Format.

.. image:: img/digitalio.png

.. list-table:: Digital IO
    :widths: 25 50
    :header-rows: 1

    * - Robot Hat V4
      - Raspberry Pi
    * - D0
      - GPIO17
    * - D1
      - GPIO4
    * - D2
      - GPIO27
    * - D3
      - GPIO22

**ADC**

.. image:: img/adcpin.png

Das Robot HAT besitzt 4 Sets von 3-Pin-ADC-Pins im P2.54-Format, gespeist mit 3,3V. Der ADC (Analog-Digital-Umsetzer) wird durch einen Mikrocontroller mit 12-Bit-Genauigkeit bereitgestellt.
Die Methode zur Auslesung des ADC-Wertes wird im Abschnitt `Onboard-Mikrocontroller` ausführlich beschrieben.

.. image:: img/btradc.png

Zudem ist der ADC-Kanal A4 über einen Spannungsteiler aus Widerständen mit dem Akku verbunden, um die ungefähre Akkuladung zu ermitteln.

Das Verhältnis des Spannungsteilers beträgt 20K/10K, daher:
A4-Spannung (Va4) = value_A4 / 4095.0 * 3.3
Batteriespannung (Vbat) = Va4 * 3
Batteriespannung (Vbat) = value_A4 / 4095.0 * 3.3 * 3

**PWM**

.. image:: img/pwmpin.png

Das Robot HAT verfügt ebenfalls über 4 Sets von 3-Pin-ADC-Pins im P2.54-Format, allerdings mit einer 5V-Stromversorgung.
Die Verwendung von PWM wird im Abschnitt `Onboard-Mikrocontroller` detailliert beschrieben.

.. note:: Die PWM-Kanäle 13 & 14 werden für den Motorantrieb genutzt.

**I2C**

.. image:: img/i2cpin.png

Das Robot HAT hat zwei I2C-Schnittstellen. Eine ist die 4-Pin-P2.54-Schnittstelle und die andere die 4-Pin-SH1.0-Schnittstelle, kompatibel mit QWIIC und STEMMA QT.
Diese I2C-Schnittstellen sind über GPIO2 (SDA) und GPIO3 (SCL) mit dem I2C-Interface des Raspberry Pi verbunden. Das Board verfügt auch über einen `Onboard-Mikrocontroller`, und beide Signalleitungen haben 10K Pull-up-Widerstände.

**SPI**

.. image:: img/spipin.png

Die SPI-Schnittstelle des Robot HAT ist eine 7-Pin-P2.54-Schnittstelle.
Sie verbindet sich mit der SPI-Schnittstelle des Raspberry Pi und beinhaltet einen zusätzlichen I/O-Pin, der für Zwecke wie Interrupts oder Resets genutzt werden kann.

.. list-table:: SPI
    :widths: 50 50
    :header-rows: 1

    * - Robot Hat V4
      - Raspberry Pi
    * - BSY
      - GPIO6
    * - CS
      - CE0(GPIO8)
    * - SCK
      - SCLK(GPIO11)
    * - MI
      - MISO(GPIO9)
    * - MO
      - MOSI(GPIO10)
    * - 3V3
      - 3,3V Versorgung
    * - GND
      - Masse



**UART**

.. image:: img/uartpin.png

Die UART-Schnittstelle des Robot HAT ist eine 4-Pin-P2.54-Schnittstelle, die mit den GPIO14 (TXD) und GPIO15 (RXD) Pins des Raspberry Pi verbunden ist.

**LED & Tasten**

Das Robot HAT ist mit einer LED und zwei Tasten ausgestattet, die alle direkt an die GPIO-Pins des Raspberry Pi angeschlossen sind.
Die RST-Taste dient bei Verwendung von Ezblock als Neustarttaste für das Ezblock-Programm. 
Wenn Ezblock nicht verwendet wird, hat die RST-Taste keine festgelegte Funktion und kann nach Ihren Bedürfnissen vollständig angepasst werden.

.. list-table:: LED & Tasten
    :widths: 50 50
    :header-rows: 1

    * - Robot Hat V4
      - Raspberry Pi 
    * - LED
      - GPIO26
    * - USR
      - GPIO25
    * - RST
      - GPIO16

**I2S-Audio**

Das Robot HAT ist mit einem integrierten I2S-Audioausgang sowie einem 2030-Audiokammer-Lautsprecher ausgestattet, der eine Mono-Ausgabe ermöglicht.

.. list-table:: I2S
    :widths: 50 50
    :header-rows: 1

    * - I2S
      - Raspberry Pi
    * - LRCLK
      - GPIO19
    * - BCLK
      - GPIO18
    * - SDATA
      - GPIO21

**Motorsteuerung**

Die Motorsteuerung des Robot HAT unterstützt zwei Kanäle und kann über zwei digitale Signale für die Richtung sowie zwei PWM-Signale für die Geschwindigkeitsregelung gesteuert werden.

.. list-table:: Motorsteuerung
    :widths: 50 50
    :header-rows: 1

    * - Motor
      - IO
    * - Motor1 Dir
      - GPIO23
    * - Motor1 Leistung
      - PWM13
    * - Motor2 Dir
      - GPIO24
    * - Motor2 Leistung
      - PWM12

**Ladeausgleich**

Erreicht eine der Batterien eine Spannung von 4,1V oder höher, während die anderen darunter liegen, wird der Ladestrom dieser speziellen Batterie reduziert.

**Batteriepegelanzeige**

Die Batteriepegelanzeige auf dem Robot HAT überwacht die Batteriespannung mittels eines Spannungsteilers und dient als Referenz zur Abschätzung des Batteriepegels.
Die Beziehung zwischen der LED und der Spannung ist wie folgt:

.. list-table:: Batteriepegel
    :widths: 50 50
    :header-rows: 1

    * - LED-Batterie
      - Gesamtspannung
    * - 2 LEDs an
      - Über 7,6V
    * - 1 LED an
      - Über 7,15V
    * - Beide LEDs aus
      - Unter 7,15V


  
**Batterie**

.. image:: img/battery.png

Das Produkt ist mit zwei in Reihe geschalteten 3,7V 18650 Lithium-Ionen-Batterien mit einer Nennkapazität von 2000mAh ausgestattet. 
Die Batterien sind über eine XH2.54 3-Pin-Schnittstelle verbunden.

* Zusammensetzung: Li-Ion (Lithium-Ion)
* Kapazität: 2000mAh, 14,8Wh
* Gewicht: 90,8g
* Anzahl der Zellen: 2
* Steckverbindung: XH2.54 3P
* Tiefentladeschutz: 6,0V

**Integrierter Mikrocontroller**

Das Robot HAT wird mit einem AT32F415CBT7-Mikrocontroller von Artery geliefert.
Es handelt sich um einen ARM Cortex-M4 Prozessor mit einer maximalen Taktfrequenz von 150MHz.
Der Mikrocontroller verfügt über 256KB Flash-Speicher und 32KB SRAM.

Die integrierten PWM und ADC werden vom Mikrocontroller gesteuert.
Die Kommunikation zwischen dem Raspberry Pi und dem Mikrocontroller erfolgt über die I2C-Schnittstelle.
Die für die Kommunikation verwendete I2C-Adresse ist 0x14 (7-Bit-Adressformat).

Register:

ADC-Lese-Wert (0x10-0x17)
  Liest den Wert des ADC. Die Daten werden im 16-Bit-Format [MSB], [LSB] zurückgelesen.
  0x17: ADC 0
  0x16: ADC 1
  ...
  0x13: ADC 4
  0x12: ADC 5 (reserviert)
  0x11: ADC 6 (reserviert)
  0x10: ADC 7 (reserviert)

PWM-Impulsbreite (0x20-0x2D)
  Setzt die Impulsbreite des PWM. Daten werden im 16-Bit-Format [MSB], [LSB] geschrieben.
  0x20: PWM 0
  0x21: PWM 1
  ...
  0x2B: PWM 11
  0x2C: PWM 12 (Motor)
  0x2D: PWM 13 (Motor)

PWM-Vorteiler (0x40-0x43)
  Legt den Vorteiler für PWM fest. Daten werden im 16-Bit-Format [MSB], [LSB] geschrieben.
  0x40: PWM Kanal 0
  0x41: PWM Kanal 1
  0x42: PWM Kanal 2
  0x43: PWM Kanal 3

PWM-Periode (0x44-0x47)
  Setzt die Periode des PWM. Daten werden im 16-Bit-Format [MSB], [LSB] geschrieben.
  0x44: PWM Kanal 0
  0x45: PWM Kanal 1
  0x46: PWM Kanal 2
  0x47: PWM Kanal 3

**PWM-Frequenz- und Periodeneinstellung**

Die PWM-Frequenz wird durch die Periode (Periode) und den Vorteiler (ARR) bestimmt. Das Prinzip basiert auf einer internen Uhr des Mikrocontrollers, die mit 72MHz läuft. Durch die Teilung der Uhr mit dem Vorteiler ergibt sich eine Frequenz (Fp). Dann kann durch Teilung von Fp durch die Periode die gewünschte Frequenz (F) berechnet werden. Daher gilt:

F = 72000000 / ARR / Periode

Im Allgemeinen ermitteln wir die Frequenz und Periode, um den Vorteiler zu berechnen. Zum Beispiel, wenn Sie einen Servomotor mit einer Frequenz von 50Hz und einer Genauigkeit von 12 Bits (Periode von 2^12, also 4096) ansteuern müssen, können Sie den Vorteiler (ARR) wie folgt berechnen:

ARR = 72000000 / F * Periode
= 72000000 / 50 / 4096
= 351,6525
≈ 352

Da ARR eine ganze Zahl sein muss, wird sie auf 352 gerundet. Daher können Sie ARR auf 352 und die Periode auf 4096 setzen, um eine tatsächliche PWM-Frequenz von etwa 49,937Hz zu erreichen, die nahe an 50Hz liegt.

Die Standardwerte für den PWM-Vorteiler (ARR) und die Periode (Periode) sind jeweils 352 und 4096, was einer Standardfrequenz von 50Hz entspricht.

**PWM-Impulsbreite**

Die Impulsbreite entspricht der Anzahl der Perioden. Wenn beispielsweise die Periode (Periode) auf 4096 eingestellt ist, 
und Sie den Impulsbreitenwert auf 2048 setzen, wird ein 50% PWM-Ausgang erzielt.

