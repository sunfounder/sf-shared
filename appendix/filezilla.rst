.. note::

    こんにちは、SunFounderのRaspberry Pi & Arduino & ESP32愛好家コミュニティへようこそ！Facebook上でRaspberry Pi、Arduino、ESP32についてもっと深く掘り下げ、他の愛好家と交流しましょう。

    **参加する理由は？**

    - **エキスパートサポート**：コミュニティやチームの助けを借りて、販売後の問題や技術的な課題を解決します。
    - **学び＆共有**：ヒントやチュートリアルを交換してスキルを向上させましょう。
    - **独占的なプレビュー**：新製品の発表や先行プレビューに早期アクセスしましょう。
    - **特別割引**：最新製品の独占割引をお楽しみください。
    - **祭りのプロモーションとギフト**：ギフトや祝日のプロモーションに参加しましょう。

    👉 私たちと一緒に探索し、創造する準備はできていますか？[|link_sf_facebook|]をクリックして今すぐ参加しましょう！

.. _filezilla:

FileZilla ソフトウェア
======================

.. image:: /_shared/appendix/img/filezilla_icon.png
   :width: 20%

ファイル転送プロトコル（FTP）は、ネットワーク上でコンピュータ間のファイルを転送するために一般的に使用されます。  
**FileZilla** は、FTP、FTPS、および **SFTP** （Raspberry Pi では推奨）をサポートするオープンソースのクライアントです。  
FileZilla を使用すると、画像・音声・スクリプトなどのファイルをコンピュータから Raspberry Pi に簡単にアップロードしたり、Pi からコンピュータへダウンロードしたりできます。

FileZilla のダウンロード
------------------------

.. |shared_link_filezilla| raw:: html

    <a href="https://filezilla-project.org/" target="_blank">FileZilla</a> 

#. |shared_link_filezilla| の公式サイトにアクセスし、お使いのオペレーティングシステム向けの **FileZilla Client** をダウンロードします。

#. プログラムをインストールして起動します。

   .. image:: /_shared/appendix/img/filezilla_install.png

#. FileZilla を開き、以下の情報を入力します。

   * **Host:** ``<hostname>.local`` または Raspberry Pi の IP アドレス  
   * **Username:** Raspberry Pi のユーザー名  
   * **Password:** Raspberry Pi Imager で設定したパスワード  
   * **Port:** ``22`` （SFTP 用）
   * **Quickconnect** をクリック（または **Enter** キーを押す）して接続します。

   .. image:: /_shared/appendix/img/filezilla_connect.png
      :align: center

#. 接続が確立されると、左側のパネルに **ローカルファイル**、右側のパネルに **Raspberry Pi のファイル** が表示されます。

    .. image:: /_shared/appendix/img/filezilla_in.png
       :align: center

#. 次の操作が可能です。

   * **アップロード**：左パネル → 右パネルにドラッグ  
   * **ダウンロード**：右パネル → 左パネルにドラッグ  

   FileZilla は直ちに転送を開始し、進行状況は下部のパネルに表示されます。
