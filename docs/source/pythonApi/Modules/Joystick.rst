.. note::

    こんにちは、SunFounderのRaspberry Pi & Arduino & ESP32愛好家コミュニティへようこそ！Facebook上でRaspberry Pi、Arduino、ESP32についてもっと深く掘り下げ、他の愛好家と交流しましょう。

    **参加する理由は？**

    - **エキスパートサポート**：コミュニティやチームの助けを借りて、販売後の問題や技術的な課題を解決します。
    - **学び＆共有**：ヒントやチュートリアルを交換してスキルを向上させましょう。
    - **独占的なプレビュー**：新製品の発表や先行プレビューに早期アクセスしましょう。
    - **特別割引**：最新製品の独占割引をお楽しみください。
    - **祭りのプロモーションとギフト**：ギフトや祝日のプロモーションに参加しましょう。

    👉 私たちと一緒に探索し、創造する準備はできていますか？[|link_sf_facebook|]をクリックして今すぐ参加しましょう！

class ``Joystick`` - 3軸ジョイスティック
========================================

**使用方法**

.. code-block:: python

    from robot_hat import Joystick, ADC, Pin

    x_pin = ADC("A0")
    y_pin = ADC("A1")
    btn_pin = Pin("D1")

    joystick = Joystick(x_pin, y_pin, btn_pin)    # ジョイスティックオブジェクトを生成
    val = joystick.read(0)                        # 軸の値を読む
    status = joystick.read_status()               # ジョイスティックの状態を読む

**コンストラクタ**

``class robot_hat.Joystick(pin)``: 与えられたピンに関連付けられたジョイスティックオブジェクトを生成します。これにより、ジョイスティックからの値を読むことができます。

**メソッド**

-  ``read`` - 指定されたピンの値を読み取り、それを返します。

.. code-block:: python

    Joystick.read(Xpin, Ypin, Btpin)

-  ``read_status`` - ジョイスティックの状態を読み取ります。

.. code-block:: python

    Joystick.read_status()

