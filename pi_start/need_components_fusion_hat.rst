.. note::

    こんにちは、SunFounderのRaspberry Pi & Arduino & ESP32愛好家コミュニティへようこそ！Facebook上でRaspberry Pi、Arduino、ESP32についてもっと深く掘り下げ、他の愛好家と交流しましょう。

    **参加する理由は？**

    - **エキスパートサポート**：コミュニティやチームの助けを借りて、販売後の問題や技術的な課題を解決します。
    - **学び＆共有**：ヒントやチュートリアルを交換してスキルを向上させましょう。
    - **独占的なプレビュー**：新製品の発表や先行プレビューに早期アクセスしましょう。
    - **特別割引**：最新製品の独占割引をお楽しみください。
    - **祭りのプロモーションとギフト**：ギフトや祝日のプロモーションに参加しましょう。

    👉 私たちと一緒に探索し、創造する準備はできていますか？[|link_sf_facebook|]をクリックして今すぐ参加しましょう！

他に何が必要ですか？
====================

このキットを使い始める前に、必要なハードウェアを準備しましょう。

必須コンポーネント
------------------

* **Raspberry Pi**

  Raspberry Pi は **頭脳** として機能し、すべての計算、センシング、制御タスクを処理します。  
  
  .. image:: /_shared/pi_start/img/need_pi.jpg

  * **対応モデル**：Raspberry Pi 5、Raspberry Pi 4、3、Raspberry Pi Zero 2W  
  * **最小構成**： **2GB RAM** — 標準的な Python プロジェクトや、OpenAI Whisper、TTS、LLM などの **オンライン AI サービス** を使用するには十分です。  
  * **推奨構成**： **4GB RAM 以上** — カメラのストリーミングや制御タスクと同時に、**ローカル AI モデル** （例：Vosk 音声認識、Piper TTS、軽量 LLM）を実行する場合でも、よりスムーズに動作します。  
  

* **電源アダプター**

  本キットには **18650 バッテリーパック** と、充電回路を内蔵した **Fusion HAT+** ボードが付属しています。
  
  .. image:: /_shared/pi_start/img/need_power.png
    :width: 400

  * 充電には、公式の **Raspberry Pi 15W USB-C アダプター** などの **5V 3A 電源** を推奨します。  
  * **USB-C Power Delivery（PD）充電器** や **QC 2.0 急速充電器** も使用できます。  
  * フル充電には通常 **約 2 時間** （0% → 100%）かかります。  


* **Micro SD カード**

  Raspberry Pi には内蔵ハードドライブがありません。起動およびすべてのファイル保存は **Micro SD カード** 上で行われます。  
  
  .. image:: /_shared/pi_start/img/need_sd.jpg
    :width: 200

  * 最小容量： **16GB**  
  * 推奨容量：安定性向上のため **32GB**  
  * ブランド：読み書きエラーを避けるため、**SanDisk** や **Samsung** など信頼性の高い製品を使用してください。  
  

オプションコンポーネント
------------------------

必須ではありませんが、以下の周辺機器を用意すると、学習やデバッグがより快適になります。

* **モニター（HDMI 対応ディスプレイまたは TV）** 

  初心者には、HDMI 入力を備えたディスプレイを強く推奨します。Raspberry Pi OS の設定や、グラフィカルなプログラムの実行が簡単になります。  

  .. image:: /_shared/pi_start/img/need_screen.png
    :width: 400

* **HDMI ケーブル（標準 / Mini / Micro）**
 
  Raspberry Pi のモデルによって使用する HDMI コネクタが異なります。お使いの Pi に対応した正しいケーブルを準備してください。 
  
  * **Raspberry Pi 4 / 5**：Micro HDMI  
  * **Raspberry Pi 3**：標準 HDMI  
  * **Raspberry Pi Zero 2W**：Mini HDMI  

  .. image:: /_shared/pi_start/img/need_hdmi.png
    :width: 400

* **キーボード & マウス**

  Raspberry Pi OS の初期設定時に非常に便利です。後から SSH や VNC によるリモートアクセスに切り替えることもできますが、初心者の方には USB またはワイヤレスの基本セットを用意することをおすすめします。  

  .. image:: /_shared/pi_start/img/need_keyboard_mouse.png
    :width: 500
 

**準備に関するヒント**

* このキットを購入した場合、多くのアクセサリーは同梱されていますが、Raspberry Pi 本体、Micro SD カード、電源アダプターは別途用意する必要があります。  
* 何を選べばよいか分からない場合、最も安定して汎用的な構成は次のとおりです：  
  **Raspberry Pi 4（2GB）＋ 公式電源アダプター ＋ 32GB Micro SD カード**  
