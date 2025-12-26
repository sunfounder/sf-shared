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

オペレーティングシステムのインストール
=======================================

.. start_imager

Raspberry Pi を使用する前に、microSD カードに **Raspberry Pi OS** をインストールする必要があります。  
このガイドでは、**Raspberry Pi Imager** を使用して、初心者にも分かりやすい方法でインストールする手順を説明します。

**必要なもの**

* コンピュータ（Windows、macOS、または Linux）
* microSD カード（16GB 以上；推奨ブランド：SanDisk、Samsung）
* microSD カードリーダー

-------------------

**1. Raspberry Pi Imager をインストールする**
----------------------------------------------

.. |shared_link_rpi_imager| raw:: html

    <a href="https://www.raspberrypi.com/software/" target="_blank">Raspberry Pi Imager</a>   

#. Raspberry Pi Imager の公式ダウンロードページ |shared_link_rpi_imager| にアクセスし、お使いのオペレーティングシステムに合ったインストーラをダウンロードします。

   .. image:: /_shared/pi_start/img/imager_download.png
      :width: 70%

#. インストール手順（言語、インストール先、確認など）に従って進めます。インストール完了後、デスクトップまたはアプリケーションメニューから **Raspberry Pi Imager** を起動します。

   .. image:: /_shared/pi_start/img/imager_install.png
      :width: 90%

-------------------

**2. microSD カードに OS を書き込む**
--------------------------------------------

1. カードリーダーを使用して、microSD カードをコンピュータに挿入します。作業を続行する前に、重要なデータは必ずバックアップしてください。

   .. image:: /_shared/pi_start/img/insert_sd.png
      :width: 90%

2. Raspberry Pi Imager を起動すると **Device** 画面が表示されます。リストから使用する Raspberry Pi のモデル（例：Raspberry Pi 5、4、3、Zero 2W）を選択します。

   .. image:: /_shared/pi_start/img/imager_device.png
      :width: 90%

   .. end_imager

3. **OS** セクションに移動し、推奨されている **Raspberry Pi OS (64-bit)** を選択します。

   .. image:: /_shared/pi_start/img/imager_os.png
      :width: 90%

   .. start_choose_os

4. **Storage** セクションで、使用する microSD カードを選択します。安全のため、他の USB ドライブは取り外し、SD カードのみが一覧に表示されるようにしてください。

   .. image:: /_shared/pi_start/img/imager_storage.png
      :width: 90%

5. **Next** をクリックして、カスタマイズ設定のステップに進みます。

   .. note::

      * モニター、キーボード、マウスを Raspberry Pi に直接接続する場合は、**SKIP CUSTOMISATION** をクリックしてもかまいません。  
      * Raspberry Pi を **ヘッドレス** （Wi-Fi 経由のリモートアクセス）でセットアップする場合は、必ずカスタマイズ設定を行ってください。

   .. image:: /_shared/pi_start/img/imager_custom_skip.png
      :width: 90%

-------------------

.. _imager_custom:

**3. OS カスタマイズ設定**
--------------------------

#. **ホスト名の設定**

   * Raspberry Pi に一意のホスト名を設定します。  
   * 後で ``hostname.local`` を使用して接続できます。

   .. image:: /_shared/pi_start/img/imager_custom_hostname.png
      :width: 90%

#. **ローカリゼーションの設定**

   * お住まいの地域の主要都市を選択します。
   * 選択内容に基づいて、タイムゾーンとキーボードレイアウトが自動設定されますが、必要に応じて変更できます。 **Next** を選択してください。
   
   .. image:: /_shared/pi_start/img/imager_custom_local.png
      :width: 90%

#. **ユーザー名とパスワードの設定**

   Raspberry Pi 用のユーザーアカウントを作成します。
   
   .. image:: /_shared/pi_start/img/imager_custom_user.png
      :width: 90%

#. **Wi-Fi の設定**

   * Wi-Fi の **SSID** （ネットワーク名）と **パスワード** を入力します。  
   * 初回起動時に Raspberry Pi が自動的に接続されます。
   
   .. image:: /_shared/pi_start/img/imager_custom_wifi.png
      :width: 90%

#. **SSH を有効化（任意・推奨）**

   * SSH を有効にすると、コンピュータからリモートでログインできます。  
   * ユーザー名／パスワードでのログイン、または SSH キーの設定が可能です。
   
   .. image:: /_shared/pi_start/img/imager_custom_ssh.png
      :width: 90%

#. **Raspberry Pi Connect を有効化（任意）**

   Raspberry Pi Connect を使用すると、Web ブラウザから Raspberry Pi のデスクトップにアクセスできます。
   
   * **Raspberry Pi Connect** をオンにし、**OPEN RASPBERRY PI CONNECT** をクリックします。
   
     .. image:: /_shared/pi_start/img/imager_custom_connect.png
        :width: 90%

   * デフォルトのブラウザで Raspberry Pi Connect の Web サイトが開きます。Raspberry Pi ID アカウントでログインするか、まだ持っていない場合は新規登録してください。

     .. image:: /_shared/pi_start/img/imager_custom_open.png
        :width: 90%

   * **New auth key** ページで、ワンタイム認証キーを作成します。
      
      * Raspberry Pi ID アカウントがどの組織にも属していない場合は、**Create auth key and launch Raspberry Pi Imager** を選択します。
      * 1 つ以上の組織に属している場合は、組織を選択してからキーを作成し、Imager を起動します。
      * キーの有効期限が切れる前に、Raspberry Pi の電源を入れ、インターネットに接続されていることを確認してください。
   
     .. image:: /_shared/pi_start/img/imager_custom_authkey.png
        :width: 90%
   
   * ブラウザから Raspberry Pi Imager を開くかどうか確認された場合は、許可してください。

     * Imager は Raspberry Pi Connect タブで起動し、認証トークンが表示されます。
     * トークンが自動的に転送されない場合は、Raspberry Pi Connect ページの **Having trouble?** セクションを開き、トークンをコピーして Imager に手動で貼り付けてください。

     .. image:: /_shared/pi_start/img/imager_custom_connect_token.png
        :width: 90%

-------------------

**4. OS イメージを書き込む**

#. すべての設定を確認し、**WRITE** をクリックします。

   .. image:: /_shared/pi_start/img/imager_writing.png
      :width: 90%

#. カードに既存のデータがある場合、デバイス上のすべてのデータが消去されるという警告が表示されます。正しいドライブが選択されていることを確認し、**I UNDERSTAND, ERASE AND WRITE** をクリックして続行します。

   .. image:: /_shared/pi_start/img/imager_erase.png
      :width: 90%

#. 書き込みと検証が完了するまで待ちます。完了すると、Raspberry Pi Imager に **Write complete!** と選択内容の概要が表示されます。ストレージデバイスは自動的に安全に取り外されます。

   .. image:: /_shared/pi_start/img/imager_finish.png
        :width: 90%

#. microSD カードを取り外し、Raspberry Pi の底面にあるスロットに挿入します。これで、新しい OS で Raspberry Pi を起動する準備が整いました。

   .. image:: /_shared/pi_start/img/os_sd_to_pi.jpg
        :width: 70%

   .. end_choose_os

