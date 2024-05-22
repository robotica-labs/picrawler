.. note::

    こんにちは、SunFounderのRaspberry Pi & Arduino & ESP32愛好家コミュニティへようこそ！Facebook上でRaspberry Pi、Arduino、ESP32についてもっと深く掘り下げ、他の愛好家と交流しましょう。

    **参加する理由は？**

    - **エキスパートサポート**：コミュニティやチームの助けを借りて、販売後の問題や技術的な課題を解決します。
    - **学び＆共有**：ヒントやチュートリアルを交換してスキルを向上させましょう。
    - **独占的なプレビュー**：新製品の発表や先行プレビューに早期アクセスしましょう。
    - **特別割引**：最新製品の独占割引をお楽しみください。
    - **祭りのプロモーションとギフト**：ギフトや祝日のプロモーションに参加しましょう。

    👉 私たちと一緒に探索し、創造する準備はできていますか？[|link_sf_facebook|]をクリックして今すぐ参加しましょう！

.. _class_i2c:

class ``i2c`` - IICバス
===========================

**使用方法**

.. code-block:: python

    from robot_hat import I2C

    i2c = I2C(1)                         # バス1上で作成
    i2c = I2C(1, I2C.MASTER)             # マスターとして作成および初期化

    i2c.send('abc')                      # 3バイト送信
    i2c.send(0x42)                       # 単一のバイトを数値で送信
    data = i2c.recv(3)                   # 3バイト受信

    i2c.is_ready(0x42)                   # スレーブ0x42が準備完了かチェック
    i2c.scan()                           # バス上のスレーブをスキャンし、有効なアドレスのリストを返す
    i2c.mem_read(3, 0x42, 2)             # スレーブ0x42のメモリから3バイト読み取る、スレーブ内のアドレス2から開始
    i2c.mem_write('abc', 0x42, 2, timeout=1000) # スレーブ0x42のメモリに'abc'（3バイト）を書き込む、スレーブ内のアドレス2から開始、1秒後にタイムアウト

**コンストラクタ**

``class robot_hat.I2C(num)``: 指定された ``num`` と関連付けられたI2Cオブジェクトを作成します。これにより、そのデバイスでI2Cを使用できます。

**メソッド**

-  ``is_ready`` - スレーブ0x42が準備完了かチェックします。

.. code-block:: python

    I2C.is_ready(addr)

-  ``scan`` - バス上のスレーブをスキャンし、リストで返します。

.. code-block:: python

    I2C.scan()

-  ``send`` - 指定したアドレスのスレーブに複数のバイトを送信します。

.. code-block:: python

    I2C.send(send, addr, timeout)

-  ``recv`` - 一つまたは複数のバイトを受信します。

.. code-block:: python

    data = i2c.recv(recv, addr, timeout)   # 3バイトを受信

-  ``mem_write`` - I2Cデバイスのメモリに書き込みます。

.. code-block:: python

    I2C.mem_write(data, addr, memaddr, timeout)

-  ``mem_read`` - I2Cデバイスのメモリから読み取ります。

.. code-block:: python

    I2C.mem_read(data, addr, memaddr, timeout)



