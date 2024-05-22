.. note::

    こんにちは、SunFounderのRaspberry Pi & Arduino & ESP32愛好家コミュニティへようこそ！Facebook上でRaspberry Pi、Arduino、ESP32についてもっと深く掘り下げ、他の愛好家と交流しましょう。

    **参加する理由は？**

    - **エキスパートサポート**：コミュニティやチームの助けを借りて、販売後の問題や技術的な課題を解決します。
    - **学び＆共有**：ヒントやチュートリアルを交換してスキルを向上させましょう。
    - **独占的なプレビュー**：新製品の発表や先行プレビューに早期アクセスしましょう。
    - **特別割引**：最新製品の独占割引をお楽しみください。
    - **祭りのプロモーションとギフト**：ギフトや祝日のプロモーションに参加しましょう。

    👉 私たちと一緒に探索し、創造する準備はできていますか？[|link_sf_facebook|]をクリックして今すぐ参加しましょう！

ハードウェア紹介
=========================

.. .. image:: img/picar_x_pic7.png

.. **モーターポート**
..     * 2チャンネルのXH2.54モーターポート。
..     * モーターポート1はGPIO 23に、モーターポート2はGPIO 24に接続されています。
..     * API: :ref:`class_motor`、左モーターポートは``0``、右モーターポートは``1``。

.. **I2Cピン**
..     * Raspberry Piからの2チャンネルI2Cピン。
..     * API: :ref:`class_i2c`

.. **PWMピン**
..     * 12チャンネルのPWMピン、P0-P12。
..     * API: :ref:`class_pwm`

.. **ADCピン**
..     * 4チャンネルのADCピン、A0-A3。
..     * API: :ref:`class_adc`

.. **デジタルピン**
..     * 4チャンネルのデジタルピン、D0-D3。
..     * API: :ref:`class_pin`

.. **バッテリーインジケーター**
..     * 電圧が7.8V以上の場合、2つのLEDが点灯します。
..     * 6.7Vから7.8Vの範囲で1つのLEDが点灯します。
..     * 6.7V以下では、両方のLEDが消灯します。

.. **LED**
..     * プログラムによって設定（1を出力で点灯、0を出力で消灯）。
..     * API: :ref:`class_pin`、``Pin("LED")``で定義可能。

.. **RSTボタン**
..     * RSTボタンを短く押すとプログラムがリセットされます。
..     * LEDが点灯するまでRSTボタンを長押し、その後解放するとBluetoothが切断されます。

.. **USRボタン**
..     * USRボタンの機能はプログラミングで設定可能（押下で“0”入力、解放で“1”入力）。
..     * API: :ref:`class_pin`、``Pin("SW")``で定義可能。

.. **電源スイッチ**
..     * ロボットHATの電源をオン/オフ。
..     * 電源ポートに電源を接続すると、Raspberry Piが起動しますが、ロボットHATを有効にするには電源スイッチをONにする必要があります。

.. **電源ポート**
..     * 7-12V PH2.0 2ピン電源入力。
..     * Raspberry PiとロボットHATを同時に給電。

.. **Bluetoothモジュール**
..     * Raspberry PiはスレーブモードでBluetoothを搭載しているため、携帯電話とのペアリングに問題があります。Raspberry PiがEzblock Studioに容易に接続できるように、別のBluetoothモジュールを追加しました。
..     * Ezblock Studioは、SunFounderがRaspberry Pi用に開発したカスタムのグラフィカルプログラミングアプリケーションです。詳細はこちら：`Ezblock Studio 3 <https://docs.sunfounder.com/projects/ezblock3/en/latest/>`_。

.. **Bluetoothインジケーター**
..     * Bluetooth接続が正常な場合は点灯し続け、接続が切断された場合は点滅し、信号が送信されている場合は高速に点滅します。

Robot Hat V4は、2つのリチウムバッテリー充電、5V/3A DC-DC放電、I2Sオーディオ出力とスピーカー、簡易バッテリーレベルインジケーター、マイクロコントローラベースのPWMとADCドライバー、さらにモータードライバーも搭載しています。

特長:
    * シャットダウン電流: < 0.5mA
    * 電源入力: USB Type-C、5V/2A
    * 充電電力: 5V/2A 10W
    * 出力電力: 5V/3A
    * 付属バッテリー: 2 x 3.7V 18650 リチウムイオンバッテリー、XH2.0 3Pインターフェース
    * バッテリー保護: 逆極性保護
    * 充電保護: 入力過電圧保護、充電バランス、過熱保護
    * 搭載充電インジケーターライト: CHG
    * 搭載電源インジケーターライト: PWR
    * 搭載2つのバッテリーレベルインジケーターLED
    * ユーザーLED、2つのタクタイルスイッチ搭載
    * モータードライバー: 5V/1.8A x 2
    * 4チャンネル 12ビットADC
    * 12チャンネルPWM
    * 4チャンネルデジタル信号
    * SPIインターフェース、UARTインターフェース、I2Cインターフェース搭載
    * モノラルスピーカー: 8Ω1W

.. list-table:: 電気的特性
   :widths: 50 25 25 25 25
   :header-rows: 1

   * - パラメーター:
     - 最小値:
     - 典型値:
     - 最大値:
     - 単位:
   * - 入力電圧:
     - 4.25
     - 5
     - 8.4
     - V
   * - バッテリー入力電圧:
     - 6.0
     - 7.4
     - 8.4
     - V
   * - 過充電保護（バッテリー）:
     -
     - 8.3
     -
     - V
   * - 入力過小電圧保護:
     - 4.15
     - 4.25
     - 4.35
     - V
   * - 入力過大電圧保護:
     - 8.3
     - 8.4
     - 8.5
     - V
   * - 充電電流（5V）:
     -
     -
     - 2.0
     - A
   * - 出力電流（5V）:
     -
     -
     - 3.0
     - A
   * - 出力電圧:
     - 5.166
     - 5.246
     - 5.327
     - V
   * - 充電過熱保護:
     - 125
     - 135
     - 145
     - °C
   * - DC-DC過熱保護:
     - 70
     - 75
     - 80
     - °C
   * - モーター出力電流:
     -
     -
     - 1.8
     - A  


詳細
----------------

**ピン & GPIO**

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
      - モーター1 DIR
      - GPIO23
    * - NC
      - 3V3    
      - モーター2 DIR
      - GPIO24
    * - SPI MOSI
      - MOSI    
      - GND
      - GND
    * - SPI MISO
      - MISO    
      - USRボタン
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
    * - MCUリセット
      - GPIO5    
      - GND
      - GND
    * - (SPI)BSY 
      - GPIO6    
      - ボード識別子2
      - GPIO12
    * - ボード識別子1
      - GPIO13    
      - GND
      - GND
    * - I2S LRCLK
      - GPIO19    
      - RSTボタン
      - GPIO16
    * - ユーザーLED
      - GPIO26    
      - NC
      - GPIO20
    * - GND
      - GND    
      - I2S SDATA
      - GPIO21



**デジタルIO**

Robot HATには、P2.54の3ピンデジタルピンが4セットあります。

.. image:: img/digitalio.png

.. list-table:: デジタルIO
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

Robot HATには、P2.54の3ピンADCピンが4セットあり、電源供給は3.3Vです。
このADC（アナログ・デジタル変換器）は、12ビット精度のマイクロコントローラによって提供されます。
ADCの値を読む方法は、「オンボードマイクロコントローラ」で詳細に説明されています。

.. image:: img/btradc.png

また、ADCチャネルA4は、抵抗器を用いた電圧分配器を介してバッテリーに接続されており、バッテリーの電圧を測定しておおよその充電状態を推定します。

分圧比は20K/10Kなので、
A4電圧（Va4）= value_A4 / 4095.0 * 3.3
バッテリー電圧（Vbat）= Va4 * 3
バッテリー電圧（Vbat）= value_A4 / 4095.0 * 3.3 * 3

**PWM**

.. image:: img/pwmpin.png

Robot HATには、P2.54の3ピンADCピンが4セットあり、電源供給は5Vです。
PWMの使用方法は、「オンボードマイクロコントローラ」で詳細に説明されています。

.. note:: PWM13および14チャネルは、モータードライブに使用されます。

**I2C**

.. image:: img/i2cpin.png

Robot HATには2つのI2Cインターフェースがあります。一つはP2.54の4ピンインターフェースで、もう一つはQWIICとSTEMMA QTと互換性のあるSH1.0の4ピンインターフェースです。
これらのI2Cインターフェースは、Raspberry PiのI2CインターフェースにGPIO2（SDA）とGPIO3（SCL）を介して接続されています。
ボードには「オンボードマイクロコントローラ」も搭載されており、2つの信号線には10Kのプルアップ抵抗があります。


**SPI**

.. image:: img/spipin.png

Robot HATのSPIインターフェースは7ピンのP2.54規格で、Raspberry PiのSPIインターフェースに接続します。さらに、割り込みやリセット等の用途に使える追加のI/Oピンも装備しています。

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
      - 3.3V電源
    * - GND
      - グラウンド

**UART**

.. image:: img/uartpin.png

Robot HATのUARTインターフェースは、4ピンのP2.54規格であり、Raspberry PiのGPIO14（TXD）およびGPIO15（RXD）に接続されます。

**LED & ボタン**

Robot HATには1つのLEDと2つのボタンが搭載され、これらは全てRaspberry PiのGPIOピンに直接接続されています。
Ezblockを使用する場合、RSTボタンはEzblockプログラムを再起動するためのものです。
それ以外の場合、RSTボタンには特定の機能は設定されていないので、自由にカスタマイズ可能です。

.. list-table:: LED & ボタン
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

**I2Sオーディオ**

Robot HATは、オンボードのI2Sオーディオ出力と、2030オーディオチャンバースピーカーを装備しており、モノラルの音声出力が可能です。

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

**モータードライバー**

Robot HATのモータードライバーは、2チャンネルに対応しており、方向制御用の2つのデジタル信号と、速度制御用の2つのPWM信号で操作します。

.. list-table:: モータードライバー
    :widths: 50 50
    :header-rows: 1

    * - モーター
      - IO
    * - Motor1 Dir
      - GPIO23
    * - Motor1 Power
      - PWM13
    * - Motor2 Dir
      - GPIO24
    * - Motor2 Power
      - PWM12

**充電バランシング**

バッテリーのうち、一つが4.1Vに達したまたは超えた場合に、その他がその閾値以下であれば、特定のバッテリーの充電電流が低減します。




**バッテリーレベルインジケータ**

Robot HATに搭載されたバッテリーレベルインジケータは、電圧分割法を使用してバッテリー電圧を監視し、バッテリーレベルの推定基準となります。
LEDと電圧との関係は以下の通りです：

.. list-table:: バッテリーレベル
    :widths: 50 50
    :header-rows: 1

    * - LEDバッテリー
      - 合計電圧
    * - 2つのLED点灯
      - 7.6V以上
    * - 1つのLED点灯
      - 7.15V以上
    * - LED両方消灯
      - 7.15V以下


**バッテリー**

.. image:: img/battery.png

本製品は、名目容量2000mAhの3.7V 18650リチウムイオンバッテリーを2個、直列接続しています。
バッテリー接続にはXH2.54 3ピンインターフェースが用いられています。

* 組成：Li-ion（リチウムイオン）
* 容量：2000mAh、14.8Wh
* 重量：90.8g
* セル数：2
* コネクタ：XH2.54 3P
* 過放電保護：6.0V


**オンボードマイクロコントローラー**

Robot HATにはArteryのAT32F415CBT7マイクロコントローラが搭載されています。
最大クロック周波数150MHzのARM Cortex-M4プロセッサで、フラッシュメモリが256KB、SRAMが32KBあります。

オンボードのPWMとADCはこのマイクロコントローラによって制御されます。
Raspberry Piとマイクロコントローラとの通信はI2Cインターフェースを介して確立され、通信に使用されるI2Cアドレスは0x14（7ビットアドレス形式）です。

レジスタ：

ADC読取値（0x10-0x17）
  ADCの値を読み取ります。データは16ビット形式[MSB]、[LSB]で読み取られます。
  0x17：ADC 0
  0x16：ADC 1
  ...
  0x13：ADC 4
  0x12：ADC 5（予約）
  0x11：ADC 6（予約）
  0x10：ADC 7（予約）

PWMパルス幅（0x20-0x2D）
  PWMのパルス幅を設定します。データは16ビット形式[MSB]、[LSB]で書き込まれます。
  0x20：PWM 0
  0x21：PWM 1
  ...
  0x2B：PWM 11
  0x2C：PWM 12（モーター）
  0x2D：PWM 13（モーター）

PWMプリスケーラ（0x40-0x43）
  PWMのプリスケーラを設定します。データは16ビット形式[MSB]、[LSB]で書き込まれます。
  0x40：PWMチャンネル 0
  0x41：PWMチャンネル 1
  0x42：PWMチャンネル 2
  0x43：PWMチャンネル 3

PWM周期（0x44-0x47）
  PWMの周期を設定します。データは16ビット形式[MSB]、[LSB]で書き込まれます。
  0x44：PWMチャンネル 0
  0x45：PWMチャンネル 1
  0x46：PWMチャンネル 2
  0x47：PWMチャンネル 3

**PWM周波数と周期設定**

PWMの周波数は周期（Period）とプリスケーラ（ARR）によって決定されます。
マイクロコントローラの内部クロックが72MHzで動作しているので、プリスケーラでクロックを分割すると、周波数（Fp）が得られます。その後、Fpを周期で割ると、目的の周波数（F）が計算できます。すなわち：

F = 72000000 / ARR / Period

通常、周波数と周期を決定してからプリスケーラを計算します。
例えば、50Hzの周波数で12ビットの精度（周期は2^12、即ち4096）のサーボモーターを駆動する必要がある場合、プリスケーラ（ARR）は以下のように計算されます：

ARR = 72000000 / F * Period
= 72000000 / 50 / 4096
= 351.6525
≈ 352

ARRは整数でなければならないため、352に四捨五入されます。したがって、ARRを352、周期を4096と設定することで、実際のPWM周波数は約49.937Hzとなり、50Hzに非常に近くなります。

PWMのプリスケーラ（ARR）と周期（Period）のデフォルト値は、それぞれ352と4096で、デフォルトの周波数は50Hzです。

**PWMパルス幅**

パルス幅は周期数に対応します。
例えば、周期（Period）が4096に設定されていて、パルス幅の値を2048に設定すると、50%のPWM出力が得られます。
