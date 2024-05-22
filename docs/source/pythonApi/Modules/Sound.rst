.. note::

    こんにちは、SunFounderのRaspberry Pi & Arduino & ESP32愛好家コミュニティへようこそ！Facebook上でRaspberry Pi、Arduino、ESP32についてもっと深く掘り下げ、他の愛好家と交流しましょう。

    **参加する理由は？**

    - **エキスパートサポート**：コミュニティやチームの助けを借りて、販売後の問題や技術的な課題を解決します。
    - **学び＆共有**：ヒントやチュートリアルを交換してスキルを向上させましょう。
    - **独占的なプレビュー**：新製品の発表や先行プレビューに早期アクセスしましょう。
    - **特別割引**：最新製品の独占割引をお楽しみください。
    - **祭りのプロモーションとギフト**：ギフトや祝日のプロモーションに参加しましょう。

    👉 私たちと一緒に探索し、創造する準備はできていますか？[|link_sf_facebook|]をクリックして今すぐ参加しましょう！

class ``Sound`` - 音センサー
============================

**使用方法**

.. code-block:: python

    from robot_hat import Sound, ADC

    pin = ADC("A0")
    sound = Sound(pin)                       # ピンからSoundオブジェクトを生成
    val = sound.read_raw()                   # アナログ値を読む

    average_val = sound.read_raw(time = 100) # 平均アナログ値を読む

**コンストラクタ**

``class robot_hat.Sound(pin)``: 与えられたピンに関連付けられたSoundオブジェクトを生成します。このオブジェクトでピンのアナログ値を読むことができます。

**メソッド**

-  ``read_raw`` - アナログピンの値を読み取り、それを返します。返される値は0から4095の範囲になります。

.. code-block:: python

    Sound.read_raw()