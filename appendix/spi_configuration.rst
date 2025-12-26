.. note::

    こんにちは、SunFounderのRaspberry Pi & Arduino & ESP32愛好家コミュニティへようこそ！Facebook上でRaspberry Pi、Arduino、ESP32についてもっと深く掘り下げ、他の愛好家と交流しましょう。

    **参加する理由は？**

    - **エキスパートサポート**：コミュニティやチームの助けを借りて、販売後の問題や技術的な課題を解決します。
    - **学び＆共有**：ヒントやチュートリアルを交換してスキルを向上させましょう。
    - **独占的なプレビュー**：新製品の発表や先行プレビューに早期アクセスしましょう。
    - **特別割引**：最新製品の独占割引をお楽しみください。
    - **祭りのプロモーションとギフト**：ギフトや祝日のプロモーションに参加しましょう。

    👉 私たちと一緒に探索し、創造する準備はできていますか？[|link_sf_facebook|]をクリックして今すぐ参加しましょう！


.. _spi_configuration:

SPI 設定
========

以下の手順に従って、Raspberry Pi で SPI インターフェースを有効化し、動作確認を行います。  
これらの手順は Raspberry Pi 5、4、3、Zero 2W に適用されます。

SPI インターフェースを有効にする
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

#. **SPI** を選択します。

   .. image:: img/ssh_spi_spi.png
      :align: center

#. **<Yes>** を選択し、続いて **<Ok> → <Finish>** を選択して変更を適用します。  
   指示が表示された場合は、Raspberry Pi を再起動してください。

   .. image:: img/ssh_spi_enable.png
      :align: center


SPI インターフェースの確認
--------------------------

#. SPI デバイスノードが存在するか確認します。

   .. code-block:: bash

      ls /dev/sp*

#. SPI インターフェースが有効な場合、次のような出力が表示されます。

   .. code-block:: text

      /dev/spidev0.0
      /dev/spidev0.1

   * これらのデバイスが表示されれば、SPI は有効で使用可能です。  
   * 表示されない場合は、Raspberry Pi を再起動してから再度確認してください。


spidev（Python 用 SPI ライブラリ）のインストール
--------------------------------------------------------

#. Python で SPI を使用するために ``spidev`` パッケージをインストールします。

   .. code-block:: bash

      sudo apt install python3-spidev

   ``spidev`` ライブラリは、 ``/dev/spidevX.Y`` インターフェースを通じて SPI デバイスへアクセスするための機能を提供します。

----------------------

これで Raspberry Pi は、コマンドラインツールおよび Python の両方を使用して SPI デバイスと通信できるように設定されました。


