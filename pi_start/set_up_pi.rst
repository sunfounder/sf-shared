.. note::

    こんにちは、SunFounderのRaspberry Pi & Arduino & ESP32愛好家コミュニティへようこそ！Facebook上でRaspberry Pi、Arduino、ESP32についてもっと深く掘り下げ、他の愛好家と交流しましょう。

    **参加する理由は？**

    - **エキスパートサポート**：コミュニティやチームの助けを借りて、販売後の問題や技術的な課題を解決します。
    - **学び＆共有**：ヒントやチュートリアルを交換してスキルを向上させましょう。
    - **独占的なプレビュー**：新製品の発表や先行プレビューに早期アクセスしましょう。
    - **特別割引**：最新製品の独占割引をお楽しみください。
    - **祭りのプロモーションとギフト**：ギフトや祝日のプロモーションに参加しましょう。

    👉 私たちと一緒に探索し、創造する準備はできていますか？[|link_sf_facebook|]をクリックして今すぐ参加しましょう！

.. _setup_pi:

Raspberry Pi をセットアップする
===============================================

Raspberry Pi のプログラミングや制御を始めるには、まずアクセスできる状態にする必要があります。  
このガイドでは、以下の 2 つの一般的な方法を紹介します。

* モニター・キーボード・マウスを使用する方法  
* ヘッドレス（画面なし）でリモート接続する方法  

.. note::

   ロボットに搭載されている Raspberry Pi Zero 2W は、画面への接続が容易ではありません。  
   **ヘッドレスセットアップ** 方法を推奨します。

-------------------------
画面がある場合
-------------------------

**必要なもの**

* Raspberry Pi
* 公式電源アダプター
* MicroSD カード
* HDMI ケーブル  
  （Raspberry Pi 4/5 の場合は、電源コネクタに最も近い **HDMI0** ポートを使用してください）
* モニター
* キーボード & マウス

**手順**

#. MicroSD カードを Raspberry Pi に挿入します。
#. キーボード、マウス、モニターを接続します。
#. Raspberry Pi の電源を入れます。
#. 起動後、Raspberry Pi OS のデスクトップが表示されます。

   .. image:: /_shared/pi_start/img/plug_screen_trixie.png
      :width: 80%
      :align: center

#. **Terminal** を開き、コマンドを入力します。

   .. image:: /_shared/pi_start/img/open_terminal.png
      :width: 80%
      :align: center


----------------------------------
画面がない場合（ヘッドレス）
----------------------------------

モニターがない場合でも、Raspberry Pi をリモートで設定・ログインできます。  
これは多くのユーザーにとって最も便利な方法です。

**必要なもの**

* Raspberry Pi
* 公式電源アダプター
* MicroSD カード
* 同じネットワーク上にあるコンピュータ

**ヒント**

* Raspberry Pi Imager を使用して OS をインストールする際に、:ref:`imager_custom` で説明されているすべての設定を完了していることを確認してください。
* Raspberry Pi とコンピュータが同じローカルネットワークに接続されていることを確認してください。
* 安定性を重視する場合は、有線 Ethernet 接続を推奨します。


**SSH で接続する**

#. コンピュータでターミナルを開きます  
   （Windows: **PowerShell**、macOS/Linux: **Terminal**）。  
   次に Raspberry Pi に接続します。

   .. code-block:: bash

      ssh <username>@<hostname>.local
      # 例:
      ssh daisy@pi.local

#. もしくは、ルーターの DHCP 一覧から Raspberry Pi の IP アドレスを確認し、次のように接続します。

   .. code-block:: bash

      ssh <username>@<IP address>
      # 例:
      ssh daisy@192.168.1.42

#. 初回ログイン時には、SSH 証明書の確認として ``yes`` を入力します。

#. Raspberry Pi Imager で設定したパスワードを入力します。  
   （入力中は何も表示されませんが、正常な動作です）

#. ログイン後、コマンドラインから完全に操作できるようになります。

   .. image:: /_shared/pi_start/img/ssh_login.png
      :align: center

----------------------

**トラブルシューティング**

* **ssh: Could not resolve hostname ...**

  * ホスト名が正しいか確認してください。
  * Raspberry Pi の IP アドレスを使って接続してみてください。

* **The term 'ssh' is not recognized...（Windows）**

  * OpenSSH がインストールされていません。手動でインストールするか、サードパーティ製の SSH クライアントを使用してください。  
  * :ref:`openssh_powershell` または :ref:`login_windows` を参照してください。

* **Permission denied (publickey,password)**

  * Raspberry Pi Imager で作成したユーザー名とパスワードを使用していることを確認してください。

* **Connection refused**

  * 電源投入後 1～2 分待ってから再接続してください。
  * Raspberry Pi Imager で SSH が有効になっていることを確認してください。

--------------------------------

グラフィカルなリモートアクセス方法
-----------------------------------

.. |shared_link_rpi_connect| raw:: html

    <a href="https://www.raspberrypi.com/documentation/services/connect.html" target="_blank">Raspberry Pi Connect</a> 

グラフィカルインターフェースを使用したい場合：

* :ref:`remote_desktop`： **VNC（Virtual Network Computing）** を有効にして、Raspberry Pi のフルデスクトップ環境を利用できます。

* |shared_link_rpi_connect|：Raspberry Pi Connect を使用すると、ブラウザから安全にどこからでもリモートアクセスできます。

これで、モニターがなくても Raspberry Pi を操作できるようになりました。  
コマンドライン操作には SSH、グラフィカルなデスクトップ操作には VNC や Raspberry Pi Connect を利用してください。
