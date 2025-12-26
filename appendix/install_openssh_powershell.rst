.. note::

    こんにちは、SunFounderのRaspberry Pi & Arduino & ESP32愛好家コミュニティへようこそ！Facebook上でRaspberry Pi、Arduino、ESP32についてもっと深く掘り下げ、他の愛好家と交流しましょう。

    **参加する理由は？**

    - **エキスパートサポート**：コミュニティやチームの助けを借りて、販売後の問題や技術的な課題を解決します。
    - **学び＆共有**：ヒントやチュートリアルを交換してスキルを向上させましょう。
    - **独占的なプレビュー**：新製品の発表や先行プレビューに早期アクセスしましょう。
    - **特別割引**：最新製品の独占割引をお楽しみください。
    - **祭りのプロモーションとギフト**：ギフトや祝日のプロモーションに参加しましょう。

    👉 私たちと一緒に探索し、創造する準備はできていますか？[|link_sf_facebook|]をクリックして今すぐ参加しましょう！

.. _openssh_powershell:

PowerShell から OpenSSH をインストールする
-----------------------------------------------------------

``ssh <username>@<hostname>.local`` または ``ssh <username>@<IP>`` を実行した際に、次のエラーが表示される場合があります。

.. code-block::

    ssh: The term 'ssh' is not recognized as the name of a cmdlet, function, script file, or operable program.

これは、Windows システムに OpenSSH がインストールされていないことを意味します。  
以下の手順に従って、手動でインストールしてください。

#. Windows のスタートメニューを開き、**powershell** と入力します。  
   **Windows PowerShell** を右クリックし、**管理者として実行** を選択します。

   .. image:: /_shared/appendix/img/powershell_ssh.png
      :align: center

#. OpenSSH クライアントをインストールします。

   .. code-block:: bash

      Add-WindowsCapability -Online -Name OpenSSH.Client~~~~0.0.1.0

#. インストール後、次のような出力が表示されます。

   .. code-block::

        Path          :
        Online        : True
        RestartNeeded : False

#. インストールを確認します。

   .. code-block:: bash

      Get-WindowsCapability -Online | Where-Object Name -like 'OpenSSH*'

#. OpenSSH が正しくインストールされていれば、次のような出力が含まれます。

   .. code-block::

        Name  : OpenSSH.Client~~~~0.0.1.0
        State : Installed
        Name  : OpenSSH.Server~~~~0.0.1.0
        State : NotPresent

   .. warning::
      ``Installed`` が表示されない場合、Windows のバージョンが古い可能性があります。  
      その場合は、サードパーティ製の SSH ツールを使用することを推奨します。詳細は :ref:`login_windows` を参照してください。

#. PowerShell を閉じてから再度開きます（今回は管理者として実行する必要はありません）。  
   その後、 ``ssh`` コマンドを使用してログインします。

   .. code-block:: bash

      ssh <username>@<hostname>.local

   .. image:: /_shared/appendix/img/powershell_login.png
      :align: center
