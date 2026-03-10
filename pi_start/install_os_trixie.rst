.. note::

    こんにちは、SunFounderのRaspberry Pi & Arduino & ESP32愛好家コミュニティへようこそ！Facebook上でRaspberry Pi、Arduino、ESP32についてもっと深く掘り下げ、他の愛好家と交流しましょう。

    **参加する理由は？**

    - **エキスパートサポート**：コミュニティやチームの助けを借りて、販売後の問題や技術的な課題を解決します。
    - **学び＆共有**：ヒントやチュートリアルを交換してスキルを向上させましょう。
    - **独占的なプレビュー**：新製品の発表や先行プレビューに早期アクセスしましょう。
    - **特別割引**：最新製品の独占割引をお楽しみください。
    - **祭りのプロモーションとギフト**：ギフトや祝日のプロモーションに参加しましょう。

    👉 私たちと一緒に探索し、創造する準備はできていますか？[|link_sf_facebook|]をクリックして今すぐ参加しましょう！

.. _install_os:

Installing the Operating System
===================================

.. start_imager

Raspberry Pi を使用する前に、**Raspberry Pi OS** を microSD カードにインストールする必要があります。  
このガイドでは、**Raspberry Pi Imager** を使用して簡単かつ初心者にも分かりやすい方法でインストールする手順を説明します。

**必要なもの**

* コンピューター（Windows、macOS、または Linux）
* microSD カード（16GB 以上推奨。推奨ブランド: SanDisk、Samsung）
* microSD カードリーダー

-------------------

1. Raspberry Pi Imager をインストールする
-------------------------------------------


.. |shared_link_rpi_imager| raw:: html

    <a href="https://www.raspberrypi.com/software/" target="_blank">Raspberry Pi Imager</a>   

#. Raspberry Pi Imager の公式ダウンロードページにアクセスします: |shared_link_rpi_imager|。使用している OS に対応するインストーラーをダウンロードします。

   .. image:: /_shared/pi_start/img/imager_download.png
      :width: 70%

#. インストール画面の指示（言語、インストール先、確認など）に従ってインストールを進めます。インストールが完了したら、デスクトップまたはアプリケーションメニューから **Raspberry Pi Imager** を起動します。

   .. image:: /_shared/pi_start/img/imager_install.png
      :width: 90%
      
--------------------------------------

.. end_imager


.. start_install_os

2. microSD カードへ OS をインストールする
------------------------------------------------

1. カードリーダーを使用して microSD カードをコンピューターに挿入します。続行する前に、重要なデータがある場合は必ずバックアップしてください。

   .. image:: /_shared/pi_start/img/insert_sd.png
      :width: 90%

2. Raspberry Pi Imager を起動すると、**Device** ページが表示されます。リストから使用する Raspberry Pi モデル（例: Raspberry Pi 5、4、3、または Zero 2W）を選択します。

   .. image:: /_shared/pi_start/img/imager_device.png
      :width: 90%

.. end_install_os

3. **OS** セクションに進み、推奨されている **Raspberry Pi OS (64-bit)** を選択します。

   .. image:: /_shared/pi_start/img/imager_os.png
      :width: 90%

.. start_setup_os

4. **Storage** セクションで microSD カードを選択します。

   .. image:: /_shared/pi_start/img/imager_storage.png
      :width: 90%

5. **Next** をクリックしてカスタマイズ設定へ進みます。

   .. note::

      * Raspberry Pi にモニター、キーボード、マウスを直接接続して使用する場合は **SKIP CUSTOMISATION** をクリックしても構いません。  
      * Raspberry Pi を **ヘッドレス** （Wi-Fi を使用したリモート接続）でセットアップする場合は、カスタマイズ設定を必ず行ってください。

   .. image:: /_shared/pi_start/img/imager_custom_skip.png
      :width: 90%

-------------------

.. _imager_custom:

3. OS カスタマイズ設定
------------------------------------------

#. **ホスト名の設定**

   * Raspberry Pi に一意のホスト名を設定します。  
   * 後で ``hostname.local`` を使って接続できます。

   .. image:: /_shared/pi_start/img/imager_custom_hostname.png
      :width: 90%

#. **ローカライゼーション設定**

   * あなたの都市（首都）を選択します。  
   * Imager が選択内容に基づいてタイムゾーンとキーボードレイアウトを自動設定します。必要に応じて変更することもできます。その後 **Next** を選択します。
   
   .. image:: /_shared/pi_start/img/imager_custom_local.png
      :width: 90%

#. **ユーザー名とパスワードの設定**

   Raspberry Pi 用のユーザーアカウントを作成します。
   
   .. image:: /_shared/pi_start/img/imager_custom_user.png
      :width: 90%

#. **Wi-Fi の設定**

   * Wi-Fi の **SSID（ネットワーク名）** と **パスワード** を入力します。  
   * Raspberry Pi は初回起動時に自動的に接続します。
   
   .. image:: /_shared/pi_start/img/imager_custom_wifi.png
      :width: 90%

#. **SSH を有効にする（任意ですが推奨）**

   * SSH を有効にすると、コンピューターからリモートログインできます。  
   * ユーザー名とパスワードでログインするか、SSH キーを設定することも可能です。
   
   .. image:: /_shared/pi_start/img/imager_custom_ssh.png
      :width: 90%

.. end_setup_os

#. **Raspberry Pi Connect を有効にする（任意）**

   Raspberry Pi Connect を使用すると、Web ブラウザから Raspberry Pi のデスクトップにアクセスできます。
   
   * **Raspberry Pi Connect** をオンにして、**OPEN RASPBERRY PI CONNECT** をクリックします。
   
     .. image:: /_shared/pi_start/img/imager_custom_connect.png
        :width: 90%

   * Raspberry Pi Connect のウェブサイトが既定のブラウザで開きます。Raspberry Pi ID アカウントでログインするか、まだアカウントを持っていない場合は新規登録してください。

     .. image:: /_shared/pi_start/img/imager_custom_open.png
        :width: 90%

   * **New auth key** ページで、ワンタイム認証キーを作成します。
      
      * Raspberry Pi ID アカウントがどの組織にも属していない場合は **Create auth key and launch Raspberry Pi Imager** を選択します。
      * 1 つ以上の組織に属している場合は組織を選択し、キーを作成して Imager を起動します。
      * キーの有効期限が切れる前に、Raspberry Pi の電源を入れてインターネットに接続してください。
   
     .. image:: /_shared/pi_start/img/imager_custom_authkey.png
        :width: 90%
   
   * ブラウザが Raspberry Pi Imager を開くかどうか確認する場合があります。その際は許可してください。

     * Imager が Raspberry Pi Connect タブで開き、認証トークンが表示されます。
     * トークンが自動的に転送されない場合は、Raspberry Pi Connect ページの **Having trouble?** セクションを開き、トークンをコピーして Imager に手動で貼り付けてください。

     .. image:: /_shared/pi_start/img/imager_custom_connect_token.png
        :width: 90%

-------------------

.. start_write_os

4. OS イメージを書き込む
-----------------------------


#. すべての設定を確認し、**WRITE** をクリックします。

   .. image:: /_shared/pi_start/img/imager_writing.png
      :width: 90%

#. カードにすでにデータが含まれている場合、Raspberry Pi Imager はデバイス上のすべてのデータが消去されるという警告を表示します。正しいドライブを選択していることを確認し、**I UNDERSTAND, ERASE AND WRITE** をクリックして続行します。

   .. image:: /_shared/pi_start/img/imager_erase.png
      :width: 90%

#. 書き込みと検証が完了するまで待ちます。完了すると Raspberry Pi Imager に **Write complete!** と表示され、設定内容の概要が表示されます。ストレージデバイスは自動的に取り出されるため、安全に取り外すことができます。

   .. image:: /_shared/pi_start/img/imager_finish.png
        :width: 90%

#. microSD カードを取り外し、Raspberry Pi 本体の裏側にあるスロットに挿入します。これで新しい OS で Raspberry Pi を起動する準備が整いました！

   .. image:: /_shared/pi_start/img/os_sd_to_pi.jpg
        :width: 70%

   .. end_write_os
