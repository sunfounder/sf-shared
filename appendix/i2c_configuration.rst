.. note::

    こんにちは、SunFounderのRaspberry Pi & Arduino & ESP32愛好家コミュニティへようこそ！Facebook上でRaspberry Pi、Arduino、ESP32についてもっと深く掘り下げ、他の愛好家と交流しましょう。

    **参加する理由は？**

    - **エキスパートサポート**：コミュニティやチームの助けを借りて、販売後の問題や技術的な課題を解決します。
    - **学び＆共有**：ヒントやチュートリアルを交換してスキルを向上させましょう。
    - **独占的なプレビュー**：新製品の発表や先行プレビューに早期アクセスしましょう。
    - **特別割引**：最新製品の独占割引をお楽しみください。
    - **祭りのプロモーションとギフト**：ギフトや祝日のプロモーションに参加しましょう。

    👉 私たちと一緒に探索し、創造する準備はできていますか？[|link_sf_facebook|]をクリックして今すぐ参加しましょう！

.. _i2c_config:

I²C 設定
========

以下の手順に従って、Raspberry Pi で I²C インターフェースを有効化し、動作確認を行います。  
これらの手順は Raspberry Pi 5、4、3、Zero 2W に適用されます。

I²C インターフェースを有効にする
----------------------------------------------

#. コンピュータでターミナルを開きます（Windows: **PowerShell**、macOS/Linux: **Terminal**）。その後、Raspberry Pi に接続します。

   .. code-block:: bash

      ssh <username>@<hostname>.local

   または：

   .. code-block:: bash

      ssh <username>@<ip_address>

#. Raspberry Pi の設定ツールを起動します。

   .. code-block:: bash

      sudo raspi-config

#. **Interfacing Options** を選択し、**Enter** を押します。

   .. image:: /_shared/appendix/img/ssh_interface.png
      :align: center

#. **I2C** を選択します。

   .. image:: img/ssh_i2c_i2c.png
      :align: center

#. **<Yes>** を選択し、続いて **<Ok> → <Finish>** を選択して変更を適用します。  
   指示が表示された場合は、Raspberry Pi を再起動してください。

   .. image:: img/ssh_i2c_yes.png
      :align: center


I²C カーネルモジュールの確認
----------------------------

#. 次のコマンドを実行します。

   .. code-block:: bash

      lsmod | grep i2c

#. I²C が有効になっている場合、次のようなモジュールが表示されます。

   .. code-block:: text

      i2c_dev        6276    0
      i2c_bcm2708    4121    0

#. 何も表示されない場合は、システムを再起動してください。

   .. code-block:: bash

      sudo reboot


i2c-tools のインストール
------------------------

#. I²C デバイスのスキャンやテストに必要なユーティリティをインストールします。

   .. code-block:: bash

      sudo apt install i2c-tools


接続された I²C デバイスの検出
------------------------------

#. I²C バスをスキャンします。

   .. code-block:: bash

      i2cdetect -y 1

#. 出力例：

   .. code-block:: text

      pi@raspberrypi ~ $ i2cdetect -y 1
          0  1  2  3   4  5  6  7  8  9   a  b  c  d  e  f
      00:           -- -- -- -- -- -- -- -- -- -- -- -- --
      10: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --
      20: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --
      30: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --
      40: -- -- -- -- -- -- -- -- 48 -- -- -- -- -- -- --
      50: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --
      60: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --
      70: -- -- -- -- -- -- -- --

#. デバイスが接続されている場合、そのアドレス（例： **0x48**）が表に表示されます。


Python 用 I²C ライブラリのインストール
--------------------------------------

#. ``python3-smbus2`` パッケージをインストールします。

   .. code-block:: bash

      sudo apt install python3-smbus2

   ``smbus2`` ライブラリは、Python で I²C デバイスと通信するために必要なすべての機能を提供します。

これで Raspberry Pi の設定は完了し、I²C デバイスと通信する準備が整いました。
