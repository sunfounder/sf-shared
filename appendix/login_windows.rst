.. note::

    こんにちは、SunFounderのRaspberry Pi & Arduino & ESP32愛好家コミュニティへようこそ！Facebook上でRaspberry Pi、Arduino、ESP32についてもっと深く掘り下げ、他の愛好家と交流しましょう。

    **参加する理由は？**

    - **エキスパートサポート**：コミュニティやチームの助けを借りて、販売後の問題や技術的な課題を解決します。
    - **学び＆共有**：ヒントやチュートリアルを交換してスキルを向上させましょう。
    - **独占的なプレビュー**：新製品の発表や先行プレビューに早期アクセスしましょう。
    - **特別割引**：最新製品の独占割引をお楽しみください。
    - **祭りのプロモーションとギフト**：ギフトや祝日のプロモーションに参加しましょう。

    👉 私たちと一緒に探索し、創造する準備はできていますか？[|link_sf_facebook|]をクリックして今すぐ参加しましょう！

.. _login_windows:

PuTTY
=========================

PuTTY は、Windows ユーザーが Raspberry Pi にリモートアクセスするための、シンプルで信頼性の高い SSH クライアントです。


.. |shared_link_putty| raw:: html

    <a href="https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html>" target="_blank">PuTTY</a> 


#. |shared_link_putty| から PuTTY をダウンロードし、コンピュータにインストールします。

   .. image:: /_shared/appendix/img/putty_download.png
      :width: 70%


#. PuTTY を起動し、接続の準備をします。

   * **Host Name** に Raspberry Pi の **ホスト名または IP アドレス** を入力します。
   * **Port** を ``22`` に設定します。
   * **Open** をクリックして接続します。


   .. image:: /_shared/appendix/img/putty_open.png
      :width: 70%
   
#. 初回使用時にセキュリティ警告が表示された場合は、**Accept** をクリックして続行します。

   .. image:: /_shared/appendix/img/putty_accept.png
      :width: 70%

#. Raspberry Pi にログインします。

   * **login as:** と表示されたら、**Raspberry Pi Imager** で設定したユーザー名を入力します。
   * パスワードを入力します（入力中は表示されませんが、正常な動作です）。
   * ログイン後、ターミナルが使用可能になり、Raspberry Pi をリモートで操作するためのコマンドを入力できます。

   .. image:: /_shared/appendix/img/putty_login.png
      :width: 70%

.. note::

    PuTTY に **inactive** と表示された場合、接続が切断されているため、再接続する必要があります。
