.. note::

    こんにちは、SunFounderのRaspberry Pi & Arduino & ESP32愛好家コミュニティへようこそ！Facebook上でRaspberry Pi、Arduino、ESP32についてもっと深く掘り下げ、他の愛好家と交流しましょう。

    **参加する理由は？**

    - **エキスパートサポート**：コミュニティやチームの助けを借りて、販売後の問題や技術的な課題を解決します。
    - **学び＆共有**：ヒントやチュートリアルを交換してスキルを向上させましょう。
    - **独占的なプレビュー**：新製品の発表や先行プレビューに早期アクセスしましょう。
    - **特別割引**：最新製品の独占割引をお楽しみください。
    - **祭りのプロモーションとギフト**：ギフトや祝日のプロモーションに参加しましょう。

    👉 私たちと一緒に探索し、創造する準備はできていますか？[|link_sf_facebook|]をクリックして今すぐ参加しましょう！

class ``TTS`` - テキストから音声へ
===================================

**使用方法**

.. code-block:: python

       from robot_hat import *

       tts = TTS()                    # TTSオブジェクトを作成
       tts.say('hello')               # 単語を発音

       # tts.write('hi')              # 単語を発音
       tts.lang('en-GB')              # 言語を変更

       tts.supported_lang()           # サポートされている言語を取得

**コンストラクタ**

``class robot_hat.TTS(engine)``: TTSオブジェクトを作成。 ``engine`` には ``"espeak"`` をEspeak、 ``"gtts"`` をGoogle TTS、 ``"polly"`` をAWS Pollyとして指定できます。

**メソッド**

-  ``say`` - TTSで単語を発音。

.. code-block:: python

       TTS.say(words)

-  ``lang`` - TTSでの言語を変更。

.. code-block:: python

       TTS.lang(language)

-  ``supported_lang`` - サポートされている全言語を照会。

.. code-block:: python

       TTS.supported_lang()

-  パラメータ調整

.. code-block:: python

       # amp: 振幅、音量
       # speed: 語速
       # gap: 間隔
       # pitch: ピッチ
       def espeak_params(self, amp=None, speed=None, gap=None, pitch=None)
