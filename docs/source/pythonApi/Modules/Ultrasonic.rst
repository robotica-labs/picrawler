.. note::

    こんにちは、SunFounderのRaspberry Pi & Arduino & ESP32愛好家コミュニティへようこそ！Facebook上でRaspberry Pi、Arduino、ESP32についてもっと深く掘り下げ、他の愛好家と交流しましょう。

    **参加する理由は？**

    - **エキスパートサポート**：コミュニティやチームの助けを借りて、販売後の問題や技術的な課題を解決します。
    - **学び＆共有**：ヒントやチュートリアルを交換してスキルを向上させましょう。
    - **独占的なプレビュー**：新製品の発表や先行プレビューに早期アクセスしましょう。
    - **特別割引**：最新製品の独占割引をお楽しみください。
    - **祭りのプロモーションとギフト**：ギフトや祝日のプロモーションに参加しましょう。

    👉 私たちと一緒に探索し、創造する準備はできていますか？[|link_sf_facebook|]をクリックして今すぐ参加しましょう！

class ``Ultrasonic`` - 超音波測距センサー
==========================================

**使用方法**

.. code-block:: python

    from robot_hat import Ultrasonic, Pin

    trig = Pin("D0")
    echo = Pin("D1")

    ultrasonic = Ultrasonic(trig, echo)       # Ultrasonicオブジェクトを生成
    val = ultrasonic.read()                   # アナログ値を読む

**コンストラクタ**

``class robot_hat.Ultrasonic(trig, echo)``: 与えられたピンに関連付けられたUltrasonicオブジェクトを生成します。このオブジェクトで距離の値を読むことができます。

**メソッド**

-  ``read`` - 距離の値を読む。

   .. code-block:: python

       Ultrasonic.read(trig, echo)