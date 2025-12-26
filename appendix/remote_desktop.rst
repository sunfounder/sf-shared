.. note::

    こんにちは、SunFounderのRaspberry Pi & Arduino & ESP32愛好家コミュニティへようこそ！Facebook上でRaspberry Pi、Arduino、ESP32についてもっと深く掘り下げ、他の愛好家と交流しましょう。

    **参加する理由は？**

    - **エキスパートサポート**：コミュニティやチームの助けを借りて、販売後の問題や技術的な課題を解決します。
    - **学び＆共有**：ヒントやチュートリアルを交換してスキルを向上させましょう。
    - **独占的なプレビュー**：新製品の発表や先行プレビューに早期アクセスしましょう。
    - **特別割引**：最新製品の独占割引をお楽しみください。
    - **祭りのプロモーションとギフト**：ギフトや祝日のプロモーションに参加しましょう。

    👉 私たちと一緒に探索し、創造する準備はできていますか？[|link_sf_facebook|]をクリックして今すぐ参加しましょう！

.. _remote_desktop:

リモートデスクトップ
====================

.. |shared_link_realvnc| raw:: html

    <a href="https://www.realvnc.com/en/connect/download/viewer/" target="_blank">RealVNC® Viewer</a>   

別のコンピュータから Raspberry Pi のデスクトップにリモートでアクセスし、操作することができます。  
推奨される方法は **VNC** で、Raspberry Pi OS で公式にサポートされており、安定した一貫性のあるデスクトップ環境を提供します。

以下のセクションでは、Raspberry Pi で VNC を有効にし、|shared_link_realvnc| を使用して接続する方法を説明します。

-----------------

VNC サービスを有効にする
------------------------

RealVNC Server は Raspberry Pi OS にプリインストールされていますが、**デフォルトでは無効** になっています。  
設定ツールから有効化する必要があります。

#. コンピュータでターミナルを開きます（Windows: **PowerShell**、macOS/Linux: **Terminal**）。その後、Raspberry Pi に接続します。

   .. code-block:: bash

      ssh <username>@<hostname>.local

   または

   .. code-block:: bash

      ssh <username>@<ip_address>

#. 設定ツールを起動します。

   .. code-block:: bash

      sudo raspi-config

   .. image:: /_shared/appendix/img/ssh_raspi_config.png


#. **Interfacing Options** を選択し、**Enter** を押します。

   .. image:: /_shared/appendix/img/ssh_interface.png


#. **VNC** を選択します。

   .. image:: /_shared/appendix/img/ssh_vnc_vnc.png


#. **Yes** を選択し、次に **OK**、最後に **Finish** を選択して終了します。

   .. image:: /_shared/appendix/img/ssh_vnc_enable.png



RealVNC® Viewer でログインする
------------------------------

#. お使いのオペレーティングシステム向けの |shared_link_realvnc| をダウンロードしてインストールします。

   .. image:: /_shared/appendix/img/ssh_vnc_download.png


#. **RealVNC Viewer** を起動し、Raspberry Pi の IP アドレスまたは ``<hostname>.local`` を入力して **Enter** を押します。

   .. image:: /_shared/appendix/img/ssh_vnc_login.png


#. Raspberry Pi の **ユーザー名** と **パスワード** を入力し、**OK** を選択します。

   .. note::

      初回接続時に「VNC Server not recognized」のようなメッセージが表示される場合があります。その場合は **Continue** を選択して続行してください。

   .. image:: /_shared/appendix/img/ssh_vnc_username.png


#. Raspberry Pi のデスクトップが表示されます。

   .. image:: /_shared/appendix/img/ssh_vnc_desktop.png


これで VNC のセットアップは完了です。

-----------------


補足事項
--------

* **デスクトップ版が必要**

  * VNC を使用するには、Raspberry Pi OS のフルデスクトップ版が必要です。  
  * **Raspberry Pi OS Lite** を使用している場合は、VNC Server を手動でインストールしてください： ``sudo apt install realvnc-vnc-server``


* **ネットワーク性能に関するヒント** 

  * 動作が遅い、または画面の更新が遅れる場合は、ネットワーク環境を確認してください。  
  * 有線 Ethernet 接続が最も高いパフォーマンスを提供します。


* **画面解像度の問題を修正する**

  * VNC ウィンドウが小さすぎる、または解像度が正しくない場合は、次の手順で固定解像度を設定してください：  
    ``sudo raspi-config`` → **Display Options** → **VNC Resolution**


* **VNC が有効になっていることを確認する**

  VNC に接続できない場合は、次の設定を確認してください：  
  ``sudo raspi-config`` → ``Interfacing Options`` → ``VNC``


* **VNC サービスを停止する**

  VNC Server を手動で停止するには、次のコマンドを実行します：  
  ``sudo systemctl stop vncserver-x11-serviced``


* **セキュリティに関する注意**

  * VNC は、信頼されたローカルネットワークでの使用を想定しています。  
  * VNC をインターネットに直接公開しないでください。  
  * ネットワーク外から安全にリモートアクセスするには、**Raspberry Pi Connect** または VPN を使用してください。
