.. note::

    こんにちは、SunFounderのRaspberry Pi & Arduino & ESP32愛好家コミュニティへようこそ！Facebook上でRaspberry Pi、Arduino、ESP32についてもっと深く掘り下げ、他の愛好家と交流しましょう。

    **参加する理由は？**

    - **エキスパートサポート**：コミュニティやチームの助けを借りて、販売後の問題や技術的な課題を解決します。
    - **学び＆共有**：ヒントやチュートリアルを交換してスキルを向上させましょう。
    - **独占的なプレビュー**：新製品の発表や先行プレビューに早期アクセスしましょう。
    - **特別割引**：最新製品の独占割引をお楽しみください。
    - **祭りのプロモーションとギフト**：ギフトや祝日のプロモーションに参加しましょう。

    👉 私たちと一緒に探索し、創造する準備はできていますか？[|link_sf_facebook|]をクリックして今すぐ参加しましょう！

class ``RGB_LED`` - rgb LED
=================================

**使用方法**

.. code-block:: python

    from robot_hat import PWM, RGB_LED

    r = PWM("P0")
    g = PWM("P1")
    b = PWM("P2")

    rgb = RGB_LED(r, g, b)                  # RGB_LEDオブジェクトを生成
    val = rgb.write('#FFFFFF')              # 16進数で色を指定して書き込む

**コンストラクタ**

``class robot_hat.RGB_LED(Rpin, Gpin, Bpin)``: 与えられたピンと関連づけられた ``RGB_LED`` オブジェクトを生成。このオブジェクトでRGB LEDの色を設定できます。
入力 ``Rpin`` , ``Gpin``, ``Bpin`` は ``robot_hat.PWM`` からの ``PWM`` オブジェクトでなければなりません。

**メソッド**

-  ``write`` - RGB LEDに特定の色を書き込む。色の値は、赤、緑、青（RGB）の16進数で表されます。各色の最小値は0（16進数で00）であり、最大値は255（16進数でFF）です。16進数の値は、#記号に続く3文字または6文字で書きます。

.. code-block:: python

    RGB_LED.write(color)