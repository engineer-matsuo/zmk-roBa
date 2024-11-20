## bluetooth対応keyball
- フォームウェアにZMKを使用
- 5個のbluetooth接続プロファイルを保持
- 有線接続にも対応。
- LiPoバッテリーを搭載し、繰り返し充電可能 
- ロータリーエンコーダ搭載


## 電源スイッチ
- 電源スイッチは下記写真の〇印の箇所にあります。上がON,下がOFFです。
<img width="544" alt="sw" src="./doc/sw.png">


## 特記事項
- 充電する際は、スイッチONの状態で行ってください。
- bluetooth接続プロファイルはキーボード上で選択、削除ができます。
- PCの設定はUS配列を推奨します。日本語配列にて使用すると、記号など設定したキーと異なる出力がされてしまうことがあります。




## キーマップの変更方法
- githubにログインしてください。アカウントをお持ちでなければ作成してください。
- このリポジトリをフォークして、自身のリポジトリとしてください。
- 初回のみ、Actionsを開いて次のボタンをクリックしてください。![image](./doc/action.png)
- [キーマップエディタ](https://nickcoutsos.github.io/keymap-editor/)でgithubと連携後、キーマップを変更し、saveボタン![image](./doc/save.png)を押してください。
- 5分程度経過するとフォームウェアの生成が完了しますので、![image](./doc/dl.png)このボタンをクリックしてください。
- 画面下部へスクロールして `firmware.zip`をダウンロード及び解凍してください。
- キーボードをPCとUSBケーブルで接続し、写真の〇印にリセットボタンがあるので、ダブルクリックしてください。<img width="544" alt="reset" src="./doc/reset.png">
- リセットボタンを押すことに慣れれば、爪楊枝やピンセット等を使用してカバーを外さずにダブルクリックができるようになります。しかし、最初はカバーを外して、そのカバーを使用してリセットボタンをクリックすることをお勧めします。
- ダブルクリックに成功すると、`XIAO-SENSE`という名前でドライブが認識されるので、作成したキーマップのフォームウェアを認識したドライブに移動させます。
- 左のキーボードには`corny_left rgbled_adapter-seeeduino_xiao_ble-zmk`、右のキーボードには`corny_right rgbled_adapter-seeeduino_xiao_ble-zmk`をドライブに移動させます。
- 数秒間でファイルの書き込みは終了し、書き込みに成功するとＰＣとの接続が勝手に解除され、フォルダは閉じられます。
- macにて書き込み操作をすると、エラーコード　‐36　等が上がりますが、無事書き込めています。
- 左右それぞれの書き込みが完了したら、キーマップが変更されていることを確認してください。
- もしBluetoothの接続に不調があれば、生成されたfirmware.zip内に格納されている`settings_reset-seeeduino_xiao_ble-zmk.uf2`を書き込んでください。初期化されますので、再度フォームウエアの書き込みをを願いします。


- レイヤー6にbluetoothプロファイルのキー配置をしています。BT_SEL0～4の切り替えで接続先デバイスの切替が可能で、BT_CLTにてプロファイル削除が可能です。
