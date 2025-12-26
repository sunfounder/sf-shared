.. note::

    こんにちは、SunFounderのRaspberry Pi & Arduino & ESP32愛好家コミュニティへようこそ！Facebook上でRaspberry Pi、Arduino、ESP32についてもっと深く掘り下げ、他の愛好家と交流しましょう。

    **参加する理由は？**

    - **エキスパートサポート**：コミュニティやチームの助けを借りて、販売後の問題や技術的な課題を解決します。
    - **学び＆共有**：ヒントやチュートリアルを交換してスキルを向上させましょう。
    - **独占的なプレビュー**：新製品の発表や先行プレビューに早期アクセスしましょう。
    - **特別割引**：最新製品の独占割引をお楽しみください。
    - **祭りのプロモーションとギフト**：ギフトや祝日のプロモーションに参加しましょう。

    👉 私たちと一緒に探索し、創造する準備はできていますか？[|link_sf_facebook|]をクリックして今すぐ参加しましょう！


.. _install_all_modules_fusion_hat:

電源設定とソフトウェアのインストール（重要）
==============================================

この章では、関連ソフトウェアのインストール、オーディオ設定、安全な電源管理の設定、および正しいシャットダウン方法について説明します。

.. start_install_fusion_hat

.. _install_fusion_hat:

``fusion-hat`` モジュールのインストール
------------------------------------------------------

このキットでは、すべての GPIO 機能は Fusion HAT+ を通して管理されます。そのため、GPIO にアクセスして制御するには、付属の ``fusion-hat`` ライブラリを使用する必要があります。

ターミナルで次のコマンドを実行し、 ``fusion-hat`` モジュールをインストールします。

   .. raw:: html

      <run></run>

   .. code-block::

      curl -sSL https://raw.githubusercontent.com/sunfounder/sunfounder-installer-scripts/main/install-fusion-hat.sh | sudo bash

.. |shared_link_fusion_hat| raw:: html

    <a href="https://docs.sunfounder.com/projects/fusion-hat/en/latest/" target="_blank">Fusion HAT+</a>

.. note:: fusion-hat の詳細については、|shared_link_fusion_hat| を参照してください。


インストールが完了したら、Raspberry Pi を再起動します。その後、オーディオ設定スクリプトを実行してください。

   .. raw:: html

      <run></run>

   .. code-block::

      sudo /opt/setup_fusion_hat_audio.sh

これで Fusion HAT+ 用ソフトウェアのインストールは完了です。


安全なシャットダウンの設定と使用
--------------------------------

Fusion HAT+ は、Raspberry Pi のシャットダウン信号を利用してシステム電源を完全に管理します。  
安全で確実な電源オフを行うために、Raspberry Pi のモデルに応じて **シャットダウン動作を設定** し、その後 **電源ボタン** を正しく使用してください。

**Raspberry Pi 5 および 4B の場合**

これらのモデルは、シャットダウン後の完全な電源オフをサポートしています。Fusion HAT+ は 3.3V ラインを監視して、Raspberry Pi の電源状態を検出します。

1. ジャンパーを **RPI_STATE → Pi3V3** に設定します。

   .. image:: /_shared/pi_start/img/state_3v3.jpg
      :width: 400

2. EEPROM 設定を手動で編集します。

   .. code-block::

      sudo raspi-config

3. **Advanced Options → A12 Shutdown Behaviour** に進みます。

   .. image:: /_shared/pi_start/img/shutdown_behaviour.png

4. **B1 Full Power Off** を選択します。

   .. image:: /_shared/pi_start/img/run_power_off.png

5. 設定を保存します。新しい設定を有効にするため、再起動を求められます。

**Raspberry Pi Zero 2W、3B、3B+ の場合**

これらのモデルは、3.3V を使用した完全な電源オフを **サポートしていません**。代わりに、GPIO26 をシャットダウン状態のインジケーターとして設定する必要があります。

1. ジャンパーを **RPI_STATE → IO26** に設定します。

   .. image:: /_shared/pi_start/img/state_io26.jpg
      :width: 400

2. ``/boot/firmware/config.txt`` ファイルを編集します。

   .. code-block::

      sudo nano /boot/firmware/config.txt

3. シャットダウン時に GPIO26 を Low、電源オン時に High に設定するため、次の行をファイル末尾に追加します。

   .. code-block::

      dtoverlay=gpio-poweroff,gpio_pin=26,active_low=1

4. 変更を反映するために再起動します。

   .. code-block::

      sudo reboot


**電源ボタンを使用した安全なシャットダウン**

シャットダウン設定が完了すると、Fusion HAT+ の電源ボタンを使用して PiCar-X を安全に電源オフできます。

* **ソフトシャットダウン（推奨）**

  * 電源ボタンを **2 秒間** 押し続けます。  
  * 2 つの電源 LED が高速で点滅します。  
  * ボタンを離す → Fusion HAT+ が Raspberry Pi のシャットダウンを開始します。  
  * シャットダウン完了後、Fusion HAT+ が自動的に電源を遮断します。  
  * これにより、SD カードやファイルが保護されます。

* **ハードシャットダウン（緊急時のみ）**

  * システムが応答しない場合、電源ボタンを **5 秒以上** 押し続けます。  
  * Fusion HAT+ が強制的に電源をオフにします。  
  * 警告：SD カードやシステムファイルが破損する可能性があります。必要な場合にのみ使用してください。

.. end_install_fusion_hat
