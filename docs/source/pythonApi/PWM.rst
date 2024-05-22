.. note::

    こんにちは、SunFounderのRaspberry Pi & Arduino & ESP32愛好家コミュニティへようこそ！Facebook上でRaspberry Pi、Arduino、ESP32についてもっと深く掘り下げ、他の愛好家と交流しましょう。

    **参加する理由は？**

    - **エキスパートサポート**：コミュニティやチームの助けを借りて、販売後の問題や技術的な課題を解決します。
    - **学び＆共有**：ヒントやチュートリアルを交換してスキルを向上させましょう。
    - **独占的なプレビュー**：新製品の発表や先行プレビューに早期アクセスしましょう。
    - **特別割引**：最新製品の独占割引をお楽しみください。
    - **祭りのプロモーションとギフト**：ギフトや祝日のプロモーションに参加しましょう。

    👉 私たちと一緒に探索し、創造する準備はできていますか？[|link_sf_facebook|]をクリックして今すぐ参加しましょう！

.. _class_pwm:

class ``PWM`` - パルス幅変調
======================================

**使用方法**

.. code-block:: python

    from robot_hat import PWM

    pwm = PWM('P0')                      # ピンからPWMオブジェクトを作成
    PWM.freq(*freq)                      # 周波数（0-65535、単位はHz）
    PWM.prescaler(*prescaler)            # プリスケーラ
    PWM.period(*arr)  
    PWM.pulse_width(*pulse_width)        # パルス幅（pulse_width < period）
    PWM.pulse_width_percent(*pulse_width_percent)  # デューティーサイクル（0-100）

**コンストラクタ**

``class robot_hat.PWM(channel)``: 指定されたピンに関連付けられたPWMオブジェクトを作成します。これにより、そのピンでpwm機能を設定できます。

**メソッド**

-  ``freq`` - pwmチャンネルの周波数を設定します。

.. code-block:: python

    PWM.freq(50)

-  ``prescaler`` - pwmチャンネルのプリスケーラを設定します。

.. code-block:: python

    PWM.prescaler(50)

-  ``period`` - pwmチャンネルの周期を設定します。

.. code-block:: python

    PWM.period(100)

-  ``pulse_width`` - pwmチャンネルのパルス幅を設定します。

.. code-block:: python

    PWM.pulse_width(10)

-  ``pulse_width_percent`` - pwmチャンネルのパルス幅のパーセンテージを設定します。

.. code-block:: python

    PWM.pulse_width_percent(50)


