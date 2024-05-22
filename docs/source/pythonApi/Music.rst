.. note::

    こんにちは、SunFounderのRaspberry Pi & Arduino & ESP32愛好家コミュニティへようこそ！Facebook上でRaspberry Pi、Arduino、ESP32についてもっと深く掘り下げ、他の愛好家と交流しましょう。

    **参加する理由は？**

    - **エキスパートサポート**：コミュニティやチームの助けを借りて、販売後の問題や技術的な課題を解決します。
    - **学び＆共有**：ヒントやチュートリアルを交換してスキルを向上させましょう。
    - **独占的なプレビュー**：新製品の発表や先行プレビューに早期アクセスしましょう。
    - **特別割引**：最新製品の独占割引をお楽しみください。
    - **祭りのプロモーションとギフト**：ギフトや祝日のプロモーションに参加しましょう。

    👉 私たちと一緒に探索し、創造する準備はできていますか？[|link_sf_facebook|]をクリックして今すぐ参加しましょう！

class ``Music`` - 音符と拍子
=================================

**使用方法**

.. code-block:: python

    from robot_hat import Music, Buzzer

    m = Music()  # Musicオブジェクトを作成
    buzzer = Buzzer("P0")
    m.tempo(120)  # 現在のテンポを1分間に120拍に設定

    # ミドルC、D、E、F、G、A、Bをそれぞれ1拍で演奏。
    buzzer.play(m.note("Middle C"), m.beat(1))
    buzzer.play(m.note("Middle D"), m.beat(1))
    buzzer.play(m.note("Middle E"), m.beat(1))
    buzzer.play(m.note("Middle F"), m.beat(1))
    buzzer.play(m.note("Middle G"), m.beat(1))
    buzzer.play(m.note("Middle A"), m.beat(1))
    buzzer.play(m.note("Middle B"), m.beat(1))

    song = './music/test.wav'
    
    m.music_set_volume(80)
    print('楽曲の長さ', m.sound_length(file_name))
    m.sound_play(song)

**コンストラクタ**

``class robot_hat.Music()``: Musicオブジェクトを作成。これにより音楽の取得や制御が可能です！

**メソッド**

-  ``note`` - 音符の周波数を取得。入力文字列は定数 ``NOTE`` でなければなりません。

.. code-block:: python

    Music.note("Middle D")
    Music.note("High A#")

-  ``beat`` - 拍子からミリ秒を取得。入力値は浮動小数点数で、例えば ``0.5`` は半拍、 ``0.25`` は4分の1拍。

.. code-block:: python

    Music.beat(0.5)
    Music.beat(0.125)

-  ``tempo`` - テンポを取得/設定、入力値はbpm（拍/分）です。

.. code-block:: python

    Music.tempo()
    Music.tempo(120)

-  ``play_tone_for`` - 音符と拍子で音を鳴らす。入力は ``Music.note("Middle D"), Music.beat(0.5)`` のようにします。

.. code-block:: python

    Music.play_tone_for(Music.note("Middle D"), Music.beat(0.5))

-  ``sound_play`` - 音楽ファイルを再生。

.. code-block:: python
    
    sound_play(file_name)

-  ``background_music`` - バックグラウンドで音楽を再生（ファイル名、ループ数、音楽ファイルの開始位置、音量）。

.. code-block:: python

    background_music(file_name, loops=-1, start=0.0, volume=50)

-  ``music_set_volume`` - 音量を設定
    
.. code-block:: python

    music_set_volume(value=50)

-  ``music_stop`` - 停止
    
.. code-block:: python

    music_stop()

-  ``music_pause`` - 一時停止
    
.. code-block:: python

    music_pause()

-  ``music_unpause`` - 一時停止解除
    
.. code-block:: python

    music_unpause()

-  ``sound_length`` - 音楽ファイルの長さを返す。
    
.. code-block:: python

    len = sound_length(file_name)
