# RFDリーダをiOS端末とHID接続中にソフトキーを利用する方法

Update: 2024/12/04

![](https://cdn.pixabay.com/photo/2014/11/12/15/48/ebook-528463_1280.jpg)

<br/>

通常、iOSとRFDリーダをHID接続するとiOS上でソフトキーが表示されなくなります。ただ、運用環境によってはソフトキーも使いたいというご要望があります。そのようなユーザ向けにHID接続をしつつ、ソフトキーを利用する方法をご案内致します。

<br/>
<br/>

### 本手順で必要なマテリアル

![1733315773441](image/myios/1733315773441.png)

1. iOS 端末
2. Windows 10 以上のPC
3. Type A <> Type CのUSBケーブル
4. Zebra RFDリーダー(Bluetooth モデル)

<br/>

### 設定手順

1. Win-PCとRFDをUSB接続する。
2. 123RFIDを起動する。123RFIDは下記リンクよりダウンロード可能。

   [123RFID デスクトップ](https://www.zebra.com/jp/ja/support-downloads/software/rfid-software/123rfid.html)
3. （推奨）123RFIDにて、RFDリーダを初期化する。

   ▽ Factory Resetを選択

   <img height="300" src="image/myios/1733313115429.png">

   <br/>
   
4. 下記設定を実行する。

   General > Bluetooth Host Type > "HID-Keyboard"を選択 > Switchを押下

   <img height="300" src="image/myios/1733313212201.png">

   <br/>

   設定が成功した場合、下記メッセージが表示されます。

   <img height="150" src="image/myios/1733313294102.png">`

   <br/>
5. 下記の設定を実行する。

   General > iOS HID Virtual Kayboard > "ENABLE"を選択

   <img height="300" src="image/myios/1733313572884.png">

   <br/>

7. 下記設定を実行する。

   Save Config > "Saved to Reader"を選択

   <img height="300" src="image/myios/1733313748525.png">

   <br/>

1. RFDからUSBケーブルを抜く。

   <br/>

### 設定の確認

1. iOS デバイスとBluetooth 接続する。
2. HIDデータを受信できるアプリを起動する。本スレッドでは"メモ"アプリを前提に説明を進める。
3. デフォルト状態ではソフトキーボードは非表示。

   <img height="300" src="image/myios/1733314323038.png">

   <br/>
4. トリガー（下）を素早く２回引くことで、ソフトキーを表示させることができる。

   ▽ 下記図の7を素早く２回引く。

   <img height="300" src="image/myios/1733314501594.png">

   <br/>

   ▽ ソフトキーが表示される。

   <img height="300" src="image/myios/1733314624520.png">

   <br/>
5. ソフトキーを非表示にする場合は、同じ要領でトリガー（下）を素早く２回引く。

   <br/>

以上
