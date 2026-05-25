.. note::

    こんにちは、SunFounderのRaspberry Pi & Arduino & ESP32愛好家コミュニティへようこそ！Facebook上でRaspberry Pi、Arduino、ESP32についてもっと深く掘り下げ、他の愛好家と交流しましょう。

    **参加する理由は？**

    - **エキスパートサポート**\ ：コミュニティやチームの助けを借りて、販売後の問題や技術的な課題を解決します。
    - **学び＆共有**\ ：ヒントやチュートリアルを交換してスキルを向上させましょう。
    - **独占的なプレビュー**\ ：新製品の発表や先行プレビューに早期アクセスしましょう。
    - **特別割引**\ ：最新製品の独占割引をお楽しみください。
    - **祭りのプロモーションとギフト**\ ：ギフトや祝日のプロモーションに参加しましょう。

    👉 私たちと一緒に探索し、創造する準備はできていますか？[|link_sf_facebook|]をクリックして今すぐ参加しましょう！

.. _cpn_fusion_hat:

Fusion HAT+
=====================================

.. image:: img/fusionhat_v0.png
    :width: 500
    :align: center
   

Fusion HAT+ は、最小限のセットアップで Raspberry Pi を完全に機能するロボットへと変換できるよう設計された、高性能で多用途な拡張ボードです。同時に、高度な自動化プロジェクトにも非常に適しています。

Fusion HAT+ の中心には、Raspberry Pi のネイティブ機能を大幅に拡張する統合マイクロコントローラー（MCU）が搭載されています。これにより、標準の Raspberry Pi には通常搭載されていない追加の PWM 出力や ADC 入力が提供されます。これにより、開発者はより精密なモーター制御と、より高度なセンサー統合を実現できます。

コンパクトなサイズにもかかわらず、Fusion HAT+ は豊富な機能を備えています。4つのモータードライバーチップを内蔵しており、最大4台のDCモーターを個別に制御することが可能です。さらに、デジタル I2S オーディオモジュールと内蔵モノラルスピーカーを搭載しており、高品質なオーディオ再生やインタラクティブなサウンド機能をボード上で直接利用できます。

このボードは、3ピンの XH2.54 コネクタを介して 6.0 V ～ 8.4 V の入力電圧を受け入れます。また、システム状態を監視するための電源ステータス LED を2つ備えており、さらにユーザーが自由にプログラムできるユーザー LED も搭載されています。加えて、オンボードボタンが用意されており、即時の機能テストや入力シミュレーションが可能です。これにより、開発およびデバッグ作業をより効率的かつ使いやすくします。

.. |link_fusion_hat| raw:: html

    <a href="https://docs.sunfounder.com/projects/fusion-hat/en/latest/" target="_blank">SunFounder Fusion HAT+</a>

詳細なガイドは次のリンクをご覧ください: |link_fusion_hat|\ 。

PinPal
============================

.. image:: img/pinpal_pic.png
    :width: 20%
    :align: center

PinPal は、SunFounder によって設計された小型のプリント基板（PCB）で、Raspberry Pi の各ピンの名称が分かりやすく印刷されています。  
Fusion HAT+ のピンヘッダーに直接取り付けることができ、プロジェクト構築中に各ピンの機能を素早く正確に確認することができます。  
これにより配線ミスを減らし、作業効率を大きく向上させます。

.. image:: img/pinpal_fusion_hat.png
    :width: 80%
    :align: center

PinPal 上の一部のピンは、**直接使用することが推奨されていません**\ 。これは、それらのピンがすでに Fusion HAT+ によって使用されているか、共有機能によって競合が発生する可能性があるためです。


#. **SDA / SCL — I2C (GPIO2 / GPIO3)**

   * Raspberry Pi のメイン I2C ピン。  
   * Fusion HAT+ は追加の P2.54 I2C ヘッダーおよび SH1.0 Qwiic / STEMMA QT ポートを提供しています。  
   * これらはすべて同じ I2C バスを共有しているため、**同時に使用できるのは1つだけです**\ 。

   .. image:: img/pinpal_i2c.png
       :width: 80%
       :align: center

#. **TXD / RXD — UART (GPIO14 / GPIO15)**

   * Raspberry Pi のメイン UART ピン。  
   * Fusion HAT+ には同じピンを使用する追加の UART コネクタがあるため、**どちらか一方のみを使用してください**\ 。

   .. image:: img/pinpal_uart.png
       :width: 80%
       :align: center

#. **GPIO 17 / 4 / 27 / 22 — 汎用 GPIO**

   * Fusion HAT+ はこれらのピンの追加セットを提供していますが、同じ Raspberry Pi GPIO にマッピングされています。  
   * **競合を防ぐため、各グループのうち1つのみを使用してください**\ 。

   .. image:: img/pinpal_gpio.png
       :width: 80%
       :align: center

#. **MOSI / MISO / SCLK / CE0 / GPIO6 — SPI ピン**

   * Fusion HAT+ は追加の SPI コネクタを提供しています。  
   * RGB コネクタ（WS2812）は MOSI ピンを使用します。  
   * **競合を避けるため、SPI グループは1つのみ使用してください。**


   .. list-table::
      :header-rows: 1

      * - Signal
        - Pin Mapping
      * - BSY
        - GPIO6
      * - CS
        - CE0 / GPIO8
      * - SCK
        - SCLK / GPIO11
      * - MI
        - MISO / GPIO9
      * - MO
        - MOSI / GPIO10

   .. image:: img/pinpal_spi.png
       :width: 80%
       :align: center


#. **GPIO 18 / 19 / 20 / 21 — I2S オーディオピン**

   * Fusion HAT+ には I2S オーディオ（スピーカー + マイク）が内蔵されています。詳細:  
     `I2S <https://docs.sunfounder.com/projects/fusion-hat/en/latest/hardware/interfaces.html#speaker-and-mic>`_。
   * これらのピンは、オーディオシステムを無効化した場合のみ再利用できます。
   * **オーディオコンポーネントが有効な間は、WS または SCLK を使用しないでください。**

   .. image:: img/pinpal_i2s.png
       :width: 80%
       :align: center

   .. list-table::
      :header-rows: 1

      * - Signal
        - Raspberry Pi Pin
      * - WS
        - GPIO19
      * - SCLK
        - GPIO18
      * - Audio OUT (Speaker)
        - GPIO21
      * - Audio IN (MIC)
        - GPIO20


#. **ID_SD / ID_SC — HAT EEPROM ピン**

   これらのピンは Raspberry Pi の HAT EEPROM 用に予約されており、拡張ボードの識別データを保存するために使用されます。  
   Fusion HAT+ はこれらのピンを内蔵 EEPROM のために使用しているため、**ID_SD (GPIO0) および ID_SC (GPIO1) を他の用途に使用することはできません**\ 。
   
   .. image:: img/pinpal_eeprom.png
       :width: 80%
       :align: center
   

