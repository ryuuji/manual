第4章 Enjuのインストール(スタンドアロンで動作させる)
====================================================

4-1 Enju仮想マシンの入手
------------------------

Enjuのインストールに必要なパッケージは，すべてネットワーク上で提供されます。

### ■Enjuパッケージの提供場所

Enjuは，以下のURLで最新版が提供されています。インストールする環境に合わせ，必要なパッケージをダウンロードします。

* [http://www.next-l.jp/download/vm/](http://www.next-l.jp/download/vm/)

![](assets/images/image_install_016.png)

#### 64bit版のEnju仮想マシンを利用する場合

WindowsコンピュータにインストールしたVirtualBox上で64bit版のEnju仮想マシンをインストールする場合，「 64bit版Enju仮想マシン 」をダウンロードしてください。ダウンロードするファイルは，以下のファイル名です。

    enju_leaf_x.x.x_vmware.zip

<div class="alert alert-info">
【Memo】<code>x.x.x</code> にはバージョン番号が表示されます。複数のパッケージが存在する場合は，最新バージョンを利用してください。
</div>

#### 32bit版のEnju仮想マシンを利用する場合

WindowsコンピュータにインストールしたVirtualBox上で32bit版のEnju仮想マシンをインストールする場合，「 32bit版Enju仮想マシン 」をダウンロードしてください。ダウンロードするファイルは，以下のファイル名です。

    enju_leaf_x.x.x_vmware_x86.zip

<div class="alert alert-info">
【Memo】<code>x.x.x</code> にはバージョン番号が表示されます。複数のパッケージが存在する場合は，最新バージョンを利用してください。
</div>

### ■パッケージの展開

Enju仮想マシンは，ダウンロードしたパッケージを展開してインストールを行います。

1. Enjuをインストールするフォルダーを作成します。  
   ![](assets/images/image_install_017.png)
2. ダウンロードした zip ファイルパッケージを展開します。  
   ![](assets/images/image_install_018.png)

4-2 VirtualBoxの設定
-----------------------

VirtualBoxを起動し，Enju仮想マシンを開く環境を設定します。

1. VirtualBoxを起動します。
2. 使用許諾に同意します。  
   ![](assets/images/image_install_025.png)
3. ［仮想マシンを開く］をクリックします。  
   ![](assets/images/image_install_026.png)
4. 前項で展開したフォルダーを選択します。
5. 「enju_ubuntu_xxxx.vmx」を選択します。  
   ![](assets/images/image_install_027.png)

   <div class="alert alert-info">
   ファイル名はEnju仮想マシンのバージョンによって異なります。
   </div>
6. ［Enju_Ubuntu_xxxx］をクリックして，［ファイル］−［Playerの環境設定］を選択します。  
   ![](assets/images/image_install_028.png)
7. ［閉じるときの動作］を選択します。
   * Enju仮想マシンのウィンドウを閉じるときの動作を選択します。選択する項目は任意です。
8. ［仮想マシンを閉じるとき］を選択します。
   * Enju仮想マシンを閉じるときの動作を選択します。選択する項目は任意です。
9. ［ソフトウェアの更新］および［ユーザーエクスペリエンス改善プログラム］を設定します。
   * オン／オフは任意です。
10. ［OK］をクリックします。  
    ![](assets/images/image_install_029.png)

    <div class="alert alert-info">
    【Memo】任意の設定項目が不明な場合，以下のように設定します。
    * ［閉じるときの動作］:［仮想マシンを閉じる前に確認画面を表示］
    * ［仮想マシンを閉じるとき］: ［パワーオフ］
    * ［ソフトウェアの更新］: オン
    * ［ユーザーエクスペリエンス改善プログラム］: オン
    </div>

4-3 Enju仮想マシンの設定
------------------------

VMwareがEnju仮想マシンに割り当てるメモリ量などの動作環境を設定します。

1. ［Enju_Ubuntu_xxxx］をクリックして，［仮想マシン］−［仮想マシンの設定］を選択します。  
   ![](assets/images/image_install_030.png)

   <div class="alert alert-info">
   仮想マシンの名前は，Enju仮想マシンのバージョンによって異なることがあります。
   </div>
2. ［ハードウェア］タブを選択します。
3. 表示された画面で，以下の推奨値を参考に各項目を設定します。
   * メモリ　　　　　　　：コンピュータに搭載されている全メモリ容量から 1 〜 2GB を減じた値
   * プロセッサ　　　　　：コンピュータに搭載されている CPU のコア数
   * ハードディスク　　　：蔵書規模に応じた値
   * ネットワークアダプタ：［NAT］を選択
4. ［OK］をクリックします。  
   ![](assets/images/image_install_031.png)

4-4 Enju仮想マシンの起動
------------------------

Enju仮想マシンを起動し，Ubuntuにログインします。

1. ［Enju_Ubuntu____］をクリックして，［仮想マシンの再生］を選択します。  
   ![](assets/images/image_install_032.png)
2. 以下のような画面が表示された場合，［コピーしました］を選択して［OK］をクリックします。  
   ![](assets/images/image_install_033.png)

   <div class="alert alert-info">
   【Memo】このメッセージ画面は，初回起動時のみ表示される場合があります。また，取外し可能デバイスの選択などが求められる場合もあります。この場合「OK」を押して先に進んでください。
   </div>
3. Ubuntuのプロンプトが表示されていることを確認します。
4. ［Ctrl］＋［G］を押して入力を仮想マシンに切り替えます。

   <div class="alert alert-info">
   VirtualBoxの画面にマウスカーソルをあわせてクリックするだけでも仮想マシンに切替ができる場合もあります。
   </div>
5. 以下の初期ユーザー名，初期パスワードでログインします。
   * 初期ユーザー名　：　enju
   * 初期パスワード　：　enjupassword  
   ![](assets/images/image_install_034.png)
6. ログインし，プロンプトが表示されていることを確認します。  
   ![](assets/images/image_install_035.png)

<div class="alert alert-info">
【Memo】VirtualBoxでキーボードから入力するときは，［Ctrl］＋［ G ］を押して仮想マシン（ゲストOS）に，［Ctrl］＋［Alt］を押してホストOSに切り替えます。
</div>

### ■キーボードの設定

使用するキーボードの種類を登録します。

1. コンピュータに接続しているキーボードの種類によって， enju@enju:~$ に続いて以下のコマンドを入力します。

   * 日本語キーボード：
         sudo loadkeys jp
   * 英語キーボード　：
         sudo loadkeys us

   enju のパスワード入力が求められますので，パスワードを打ち込んでください(画面には出力されません)。

2. パスワード（初期パスワード：enjupassword）を入力します。  
   ![](assets/images/image_install_036.png)

<div class="alert alert-info">
場合によっては，「<code>unknown charset unicode - ignoreing charset request</code>」などと表示され，キーボード上の配置が変更されないこともあるようです。ただし，サーバ上で記号を使うすることがなければ，大きな問題はありませんので，そのまま続けてください。ただし，キーボードの記号(!"#$%&'()など)が正しく入力されていない状況では，次項のパスワード中には記号は含めないようにしてください。
</div>

### ■パスワードの変更

初期ユーザー名「Enju」に対するパスワードを変更します。

1. enju@enju:~$ に続いて以下のコマンドを入力します。

       passwd

2. 現在のパスワード，新しいパスワード，新しいパスワード（確認）の順に入力します。  
   ![](assets/images/image_install_037.png)

### ■IPアドレスの確認と設定

Enju仮想マシンの設定時に，ネットワークアダプタを「 NAT(ホストのIPアドレスを共有して使用) 」と設定しましたので，Enju仮想マシンに対しては自動的に適切なIPアドレスが割り当てられています。

そこで，まず割り当てられたIPアドレスを確認し，これを Enjuサーバが認識できるように設定する必要があります。

1. enju@enju:~$ に続いて以下のコマンドを入力します。

       ifconfig

   etho (または eth1)のところに書かれている inet addr: の値をメモします。以下の画面では，<code>192.168.112.128</code>です。  
   ![](assets/images/image_install_041.png)

   <div class="alert alert-info">
   もし，画面が流れていって，読めない場合には <kbd>ifconfig | more</kbd> と入力してください。
   </div>

2. enju@enju:~$ に続いて以下のコマンドを入力します。

       ruby setip.rb IP_addr

   「IP_addr」に固定するIPアドレスの値として，前項でメモしたIPアドレスを入力します。下の画面では192.168.13.11を指定していますが，これをそのまま打ち込むのではなく，必ず前項でメモした値を指定してください。  
   ![](assets/images/image_install_038.png)

### ■Enju仮想マシンの起動

Enju仮想マシンを起動します。

1. enju@enju:~$ に続いて以下のコマンドを入力します。

       sudo enju start

   enju のパスワード入力が求められますので，パスワードを打ち込んでください(画面には出力されません)。  
   ![](assets/images/image_install_078.png)

2. 画面上に何か文字列が表示されただけで， enju@enju:~$ という文字列が表示され，本当に正しく動いているのかどうかわかりにくいですが，正しく動いている場合でも上記のようになります。

   **VirtualBox上でNext-L Enjuが動作している間，VirtualBoxは閉じてはいけません。もし，画面上で邪魔だと感じる場合は，アイコン化(最小化)した状態としておいてください。**

4-5 Enju仮想マシンが正しく起動されているかの確認
------------------------------------------------

Next-L Enjuが正しく起動したかどうかは，サーバ上だけではわかりにくいので，ネットワークに接続された別のコンピュータから確認します。別のマシンといっても，物理的に別のマシンを使うのではなく，Next-L Enjuが動作している同じコンピュータのWebブラウザを用いて確認を行います。なすなわち，ゲストOS(今回の場合はVirtualBox中のEnju仮想マシン)とホストOS(ここではVMwareが動作しているWindows)とは論理的には別のマシンと見なすことができますので，Windows上のWebブラウザを使って確認すれば良いことになります。

1. ホストOS(Windows)に制御を戻します。
   「Ctrl」 + 「Alt」 キーを押します。
   「Ctrl」 + 「Alt」キーを押すと，それまで表示されていなかったマウスカーソルが再度表示されます。
2. ブラウザからアクセスします。

   Windows上でWebブラウザを立ち上げ，アドレス欄に，「http://仮想マシンに割り当てたに割り当てたIPアドレス」と入力してください。たとえば，前項の例では 192.168.112.128 というIPアドレスを仮想マシンに割り当てていた場合には，アドレス欄に以下のように入力することになります。
       http://192.168.1.128

これで，同じPC上からも，また別のマシンからもEnjuサーバに対してアクセスすることが可能になったと思います。このようにアクセスしても正しく画面が表示されない場合には，何らかの設定ミスがあると思われますので，再度インストールしなおしてください。

4-6 Enjuサーバの停止と再起動
-----------------------------

### ■Enju サーバのシャットダウン

Enjuサーバを終了(シャットダウン)させる場合には，正しい手順でのシャットダウンを行う必要があり，VirtualBoxをいきなり終了させたり，PCの電源ボタンを押すなどして強制終了させると，使用中のデータベースファイルが壊れて，再起動できなくなるなどの問題が発生する可能性があります。

1. enju@enju:~$ に続いて以下のコマンドを入力します。

       sudo enju stop
2. enju@enju:~$ に続いて以下のコマンドを入力します。

       sudo shutdown -h now

   これらでenju のパスワード入力が求められますので，パスワードを打ち込んでください(画面には出力されません)。

Enjuサーバをシャットダウンするタイミングは，図書館の運用方針で決定することができます。システム的には，起動したら基本的にはずっと動作させ続けていても問題ありません。毎日システムをシャットダウンする，必要な時だけ稼働させるなど，ポリシーに応じた運用をすることができます。

### ■Enju サーバの再起動

1. VirtualBoxが終了していた場合，再度VirtualBoxを起動してください。  
   ![](assets/images/image_install_079.png)
2. VirtualBoxが起動後，「 enju_ubuntu_xxxx 」を指定して「仮想マシンの再生」を選択してください。  
   ![](assets/images/image_install_080.png)
3. 再起動して，ユーザ名とパスワードの入力が求められますので，ユーザー名( enju )と，前に変更したパスワードを入力してログインしてください。  
   ![](assets/images/image_install_034.png)
4. enju@enju:~$ に続いて，以下のコマンドを入力します。パスワードの入力が求められることがあります。

       sudo enju start

これで，再度Enjuサーバが利用できるようになりました。