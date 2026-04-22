.. note::

    こんにちは、SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasts Community on Facebookへようこそ！他の愛好家と一緒に、Raspberry Pi、Arduino、ESP32の世界により深く入り込みましょう。

    **参加する理由**

    - **専門家サポート**: 購入後の問題や技術的な課題を、コミュニティと私たちのチームの助けを借りて解決します。
    - **学習と共有**: ヒントやチュートリアルを交換して、スキルを向上させましょう。
    - **限定プレビュー**: 新製品の発表や先行プレビューに早期アクセスできます。
    - **特別割引**: 最新製品を特別割引でお楽しみいただけます。
    - **季節限定キャンペーンとプレゼント**: プレゼント企画やホリデーキャンペーンに参加しましょう。

    👉 一緒に発見し、創造する準備はできましたか？ [|link_sf_facebook|] をクリックして、今すぐ参加しましょう！

.. _install_os:

オペレーティングシステムのインストール
=================================================

.. start_imager

Raspberry Piを使用する前に、microSDカードに **Raspberry Pi OS** をインストールする必要があります。  
このガイドでは、**Raspberry Pi Imager** を使用して、初心者にもわかりやすい方法で行う方法を説明します。

**必要なコンポーネント**

* コンピューター（Windows、macOS、またはLinux）
* microSDカード（16GB以上、推奨ブランド：SanDisk、Samsung）
* microSDカードリーダー

-------------------

Raspberry Pi Imagerのインストール
-------------------------------------------

.. |shared_link_rpi_imager| raw:: html

    <a href="https://www.raspberrypi.com/software/" target="_blank">Raspberry Pi Imager</a>   

#. 公式Raspberry Pi Imagerダウンロードページ（|shared_link_rpi_imager|）にアクセスします。お使いのオペレーティングシステムに適したインストーラーをダウンロードしてください。

   .. image:: /_shared/pi_start/img/imager_download.png
      :width: 70%

#. インストールの指示（言語、インストールパス、確認）に従います。インストール後、デスクトップまたはアプリケーションメニューから **Raspberry Pi Imager** を起動します。

   .. image:: /_shared/pi_start/img/imager_install.png
      :width: 90%
      
--------------------------------------

.. end_imager


.. start_install_os

microSDカードへのOSインストール
------------------------------------------------

1. カードリーダーを使用して、microSDカードをコンピューターに挿入します。続行する前に、重要なデータをバックアップしてください。

   .. image:: /_shared/pi_start/img/insert_sd.png
      :width: 90%

2. Raspberry Pi Imagerを開くと、**Device** ページが表示されます。リストからお使いのRaspberry Piモデルを選択します（例：Raspberry Pi 5、4、3、またはZero 2W）。

   .. image:: /_shared/pi_start/img/imager_device.png
      :width: 90%

.. end_install_os

3. **OS** セクションに移動し、推奨される **Raspberry Pi OS (64-bit)** オプションを選択します。

   .. image:: /_shared/pi_start/img/imager_os.png
      :width: 90%


.. start_storage

4. **Storage** セクションで、microSDカードを選択します。

   .. image:: /_shared/pi_start/img/imager_storage.png
      :width: 90%

.. end_storage

-------------------

.. _imager_custom:

.. start_cutomization_os

OSカスタマイズ設定
------------------------------------------

#. カスタマイズ手順に進みます。

   * モニター、キーボード、マウスをRaspberry Piに直接接続する場合は、**SKIP CUSTOMISATION** をクリックしてください。
   * Raspberry Piを*ヘッドレス*（Wi-Fiリモートアクセス）でセットアップする予定の場合は、カスタマイズ設定を完了する必要があります。

   .. image:: /_shared/pi_start/img/imager_custom_skip.png
      :width: 90%

#. **ホスト名の設定**

   * Raspberry Piに固有のホスト名を付けます。
   * 後で ``ホスト名.local`` を使用して接続できます。

   .. image:: /_shared/pi_start/img/imager_custom_hostname.png
      :width: 90%

#. **ローカライゼーションの設定**

   * あなたの国の主要な都市を選択します。
   * Imagerはあなたの選択に基づいてタイムゾーンとキーボードレイアウトを自動的に補完します。必要に応じて調整することも可能です。Nextを選択してください。

   .. image:: /_shared/pi_start/img/imager_custom_local.png
      :width: 90%

#. **ユーザー名とパスワードの設定**

   Raspberry Pi用のユーザーアカウントを作成します。

   .. image:: /_shared/pi_start/img/imager_custom_user.png
      :width: 90%

#. **Wi-Fiの設定**

   * Wi-Fiの **SSID**（ネットワーク名）と **パスワード** を入力します。
   * Raspberry Piは初回起動時に自動的に接続します。

   .. image:: /_shared/pi_start/img/imager_custom_wifi.png
      :width: 90%

#. **SSHの有効化（オプションですが推奨）**

   * SSHを有効にすると、コンピューターからリモートログインできるようになります。
   * ユーザー名とパスワードを使用してログインするか、SSHキーを設定できます。

   .. image:: /_shared/pi_start/img/imager_custom_ssh.png
      :width: 90%

.. end_cutomization_os

.. start_enable_connection

#. **Raspberry Pi Connectの有効化（オプション）**

   Raspberry Pi Connectを使用すると、WebブラウザーからRaspberry Piデスクトップにアクセスできます。

   * **Raspberry Pi Connect** をオンにし、**OPEN RASPBERRY PI CONNECT** をクリックします。

     .. image:: /_shared/pi_start/img/imager_custom_connect.png
        :width: 90%

   * Raspberry Pi Connectのウェブサイトがデフォルトのブラウザーで開きます。Raspberry Pi IDアカウントにログインするか、まだアカウントをお持ちでない場合はサインアップしてください。

     .. image:: /_shared/pi_start/img/imager_custom_open.png
        :width: 90%

   * **New auth key** ページで、ワンタイム認証キーを作成します。

      * あなたのRaspberry Pi IDアカウントがいかなる組織にも属していない場合は、**Create auth key and launch Raspberry Pi Imager** を選択してください。
      * 1つ以上の組織に属している場合は、そのいずれかを選択し、キーを作成してImagerを起動してください。
      * キーの有効期限が切れる前に、Raspberry Piの電源を入れ、インターネットに接続してください。

     .. image:: /_shared/pi_start/img/imager_custom_authkey.png
        :width: 90%

   * ブラウザーがRaspberry Pi Imagerを開くよう求める場合があります — 許可してください。

     * ImagerがRaspberry Pi Connectタブで開き、認証トークンが表示されます。
     * トークンが自動的に転送されない場合は、Raspberry Pi Connectページの **Having trouble?** セクションを開き、トークンをコピーしてImagerに手動で貼り付けてください。

     .. image:: /_shared/pi_start/img/imager_custom_connect_token.png
        :width: 90%

.. end_enable_connection

-------------------

.. start_write_os

OSイメージの書き込み
-----------------------------

#. すべての設定を確認し、**WRITE** をクリックします。

   .. image:: /_shared/pi_start/img/imager_writing.png
      :width: 90%

#. カードにすでにデータが存在する場合、Raspberry Pi Imagerはデバイス上のすべてのデータが消去されるという警告を表示します。正しいドライブを選択したことを再確認し、**I UNDERSTAND, ERASE AND WRITE** をクリックして続行します。

   .. image:: /_shared/pi_start/img/imager_erase.png
      :width: 90%

#. 書き込みと検証が完了するまで待ちます。完了すると、Raspberry Pi Imagerは **Write complete!** とあなたの選択の概要を表示します。ストレージデバイスは自動的に取り出されるため、安全に取り外すことができます。

   .. image:: /_shared/pi_start/img/imager_finish.png
        :width: 90%

#. microSDカードを取り外し、Raspberry Piの裏面のスロットに挿入します。これで、新しいOSでRaspberry Piを起動する準備が整いました！

   .. image:: /_shared/pi_start/img/os_sd_to_pi.jpg
        :width: 70%

   .. end_write_os