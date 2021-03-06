## [RN4020](https://www.microchip.com/en-us/product/RN4020) OEM モジュール インターフェイス について

### コマンド

| 種類    | 利用優先度 | コマンド名                                 | 説明                                                                                                                                                                                     |
| :------ | :--------: | :----------------------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Set/Get |     低     | S-,\<string>                               | シリアル化した名称                                                                                                                                                                       |
| ^       |     低     | SB,\<0-7><br>GB                            | UART baud レートを設定                                                                                                                                                                   |
| ^       |     低     | SDF,\<text><br>GDF                         | ファームウェア リビジョンを設定                                                                                                                                                          |
| ^       |     低     | SDH,\<text><br>GDH                         | ハードウェア リビジョンを設定                                                                                                                                                            |
| ^       |     低     | SDM,\<text><br>GDM                         | モデル名を設定                                                                                                                                                                           |
| ^       |     低     | SDN,\<text><br>GDN                         | メーカー名を設定                                                                                                                                                                         |
| ^       |     低     | SDR,\<text><br>GDR                         | ソフトウェア リビジョンを設定                                                                                                                                                            |
| ^       |     低     | SDS,\<text><br>GDS                         | シリアル番号を設定                                                                                                                                                                       |
| ^       |     中     | SF,\<1,2>                                  | 工場出荷時の既定値にリセット<br>1 : デバイス名,デバイス情報,スクリプト,プライベート サービス等一部の設定以外を工場出荷時の既定値に戻す<br>2 : 全てのパラメータを工場出荷時の既定値に戻す |
| ^       |     低     | SM,\<1-3>,\<hex32>                         | タイマの時間を μs で設定                                                                                                                                                                 |
| ^       |     低     | SN,\<string><br>GN                         | デバイス名を設定                                                                                                                                                                         |
| ^       | <b>高</b>  | SR,\<hex32><br>GR                          | 機能を設定 (参照：機能のビットパターン)                                                                                                                                                  |
| ^       | <b>高</b>  | SS,\<hex32><br>GS                          | サーバサービスを設定 (参照：サービスのビットパターン)                                                                                                                                    |
| ^       |     中     | ST,\<interval>,\<latency>,\<timeout><br>GT | 接続パラメータを設定                                                                                                                                                                     |


| 種類       | 利用優先度 | コマンド名                          | 説明                         |
| :--------- | :--------: | :---------------------------------- | :--------------------------- |
| アクション |     中     | +                                   | エコー                       |
| ^          |     低     | @O,\<0-2>,\<hex16>                  | アナログ信号を出力           |
| ^          |     低     | @I,\<0-2>                           | アナログ信号を入力           |
| ^          |     低     | \|O,\<hex8>,\<hex8>                 | PIO の出力を設定             |
| ^          |     低     | \|I,\<hex8>                         | PIO の入力を取得             |
| ^          |     中     | A,\<hex16>,\<hex16>                 | アドバタイズを開始           |
| ^          |     中     | B,\<0,1>                            | ボンディング                 |
| ^          |     低     | D                                   | 設定内容をダンプ出力         |
| ^          |     中     | E,\<0,1>,\<mac address>             | 接続を確立                   |
| ^          |     中     | F,\<hex16>,\<hex16>                 | スキャン開始                 |
| ^          |     低     | H                                   | ヘルプ                       |
| ^          |     中     | J,\<0,1>                            | オブザーバロールの開始と終了 |
| ^          |     中     | K                                   | 切断                         |
| ^          |     中     | M                                   | ピアから RSSI を取得         |
| ^          |     中     | N,\<hex>                            | ブロードキャスト情報を入力   |
| ^          |     中     | O                                   | 休止ステートへ移行           |
| ^          |     中     | R,1                                 | 再起動                       |
| ^          |     中     | T,\<interval>,\<latency>,\<timeout> | 現在の接続パラメータを変更   |
| ^          |     中     | U                                   | ボンディング解除             |
| ^          |     中     | V                                   | ファームウェア バージョン    |
| ^          |     中     | X                                   | スキャン停止                 |
| ^          |     中     | Y                                   | アドバタイズ停止             |
| ^          |     中     | Z                                   | 接続停止                     |


| 種類     | 利用優先度 | コマンド名 | 説明                                                                  |
| :------- | :--------: | :--------- | :-------------------------------------------------------------------- |
| サービス |     低     | LC         | クライアント サービスをリスト表示                                     |
| ^        |     低     | LS         | サーバサービスをリスト表示                                            |
| ^        |     低     | CHR        | クライアント ハンドルから値を読み出し                                 |
| ^        |     低     | CHW        | クライアント ハンドルの値を書き込み                                   |
| ^        |     低     | CURC       | クライアント UUID の設定を読み出し                                    |
| ^        |     低     | CURV       | クライアント UUID の値を読み出し                                      |
| ^        |     低     | CUWC       | クライアント UUID のノーティフィケーション / インディケーションを開始 |
| ^        |     低     | CUWV       | クライアント UUID へ値を書き込み                                      |
| ^        |     低     | SHR        | サーバハンドルの値を読み出し                                          |
| ^        | <b>高</b>  | SHW        | サーバハンドルへ値を書き込み                                          |
| ^        |     低     | SUR        | サーバ UUID の値を読み出し                                            |
| ^        | <b>高</b>  | SUW        | サーバ UUID へ値を書き込み                                            |


| 種類                 | 利用優先度 | コマンド名                | 説明                                              |
| :------------------- | :--------: | :------------------------ | :------------------------------------------------ |
| プライベートサービス |     低     | PC,\<hex32>,\<xxx>,\<xxx> | プライベート キャラクタリスティックの UUID を設定 |
| ^                    |     低     | PS,\<hex32>               | プライベート サービスの UUID を設定               |
| ^                    |     低     | PZ                        | プライベート サービスをクリア                     |
| MLDP                 | <b>高</b>  | SE,\<0-2>                 | MLDP のセキュリティ モードを設定                  |
| ^                    | <b>高</b>  | I                         | MLDP モードを開始                                 |
| スクリプト機能       |     中     | LW                        | スクリプトを表示                                  |
| ^                    |     中     | WC                        | スクリプトをクリア                                |
| ^                    |     中     | WP                        | スクリプトを停止                                  |
| ^                    |     中     | WR,\<0-9>                 | スクリプトを実行                                  |
| ^                    |     中     | WW                        | スクリプトを書き込み                              |
| リモート             |     中     | !,\<0,1>                  | リモートコマンド モードを開始                     |
| DFU                  |     低     | ~,\<1,2>                  | デバイス ファームウェアを更新                     |


#### 機能のビットパターン

| サービス                                  | ビットパターン | 説明                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| ----------------------------------------- | -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Central                                   | 0x80000000     | このビットをセットした場合、デバイスはセントラルとして接続を開始します。このビットをクリアした場合、デバイスはペリフェラルとしてアドバタイズを開始します。Real-time Read 0x40000000 このビットをセットした場合、デバイスは UART 経由でホスト MCU に対して値を要求し、ホスト MCU はタイムリーに応答する必要があります。このビットをクリアした場合、デバイスは RN4020 の RAM に保存されているキャラクタリスティック値を読み出します。Auto Advertise 0x20000000 この設定はペリフェラル デバイスにのみ適用されます。このビットをセットした場合、デバイスはパワーサイクル、再起動、切断後にアドバタイズを開始します。このビットをクリアした場合、デバイスはコマンドモードでUART からコマンド「A」を受信した後にアドバタイズを開始します。 |
| Support MLDP                              | 0x10000000     | このビットをセットした場合、デバイスは Bluetooth LE上でシリアルデータの非同期転送を行うプライベートサービス MLDP をサポートします。このビットをクリアした場合、MLDP は無効です。詳細は、セクション 2.2.5「Microchip MLDP コマンド」を参照してください。                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Auto MLDP Disable                         | 0x08000000     | この設定は、MLDP が有効な場合のみ有効です。このビットをセットした場合、コマンドモードで UART からコマンド「I」を受信するか、CMD/MLDP( ピン 8) を Highにするとデバイスは MLDP モードになります。このビットをクリアした場合、コマンド「I」または CMD/MLDPピンによるだけでなく、ピアデバイスから MLDP データストリームを受信した場合もデバイスはMLDPモードになります。                                                                                                                                                                                                                                                                                                                                                                  |
| No Direct Advertisement                   | 0x04000000     | この設定はペリフェラル デバイスの場合のみ有効です。このビットをセットした場合、ペリフェラルはボンディング済みであっても不特定多数に向けたアドバタイズを発行します。従って、アドバタイズ中はいつでも検出可能です。この設定は、iOS または Android 機器と接続する場合に役立ちます。                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| UART Flow Control                         | 0x02000000     | この設定は RN4020 モジュールの UART ポートのRTS/CTS ハードウェア フロー制御の制御に使います。このビットをセットした場合、フロー制御が有効で、ホストは UART ハードウェア フロー制御機能をサポートする必要があります。MLDP を有効にした場合、フロー制御が必要です。                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Run Script After Power On                 | 0x01000000     | この設定はスクリプト実行の制御に使います。このビットをセットした場合、@PW_ON イベントが生成されスクリプト実行が起動後自動的に開始します。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| 予約済み                                  | 0x00800000     | -                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Enable Authentication                     | 0x00400000     | この設定は、接続時に認証を有効にして中間者 (MITM)攻撃を防ぎます。認証を有効にした場合、I/O 機能としてキーボードとディスプレイのどちらかまたは両方を設定する必要があります。詳細は、Bluetooth コア仕様v4.1 Vol 3、Part H、Section 2.3.5.1「Selecting STKGeneration Method」の Table 2.5「Mapping of IOCapabilities to STK Generation Method」を参照してください。                                                                                                                                                                                                                                                                                                                                                                     |
| Enable Remote Command                     | 0x00200000     | この設定は MLDP 機能が有効な場合のみ有効です。このビットをセットした場合、ローカルデバイスは MLDPデータストリームを利用してリモートデバイスからのリモートコマンド受信、およびリモートデバイスへのコマンド出力送信が可能です。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Do not Save Bonding                       | 0x00100000     | このビットをセットした場合、ボンディング情報は NVMに保存されずボンディングは現在の接続に対してのみ有効です。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| I/O Capabilities                          | 0x000E0000     | モジュールの I/O 機能です。Enable Authentication ビットをセットした場合のみ有効です。<br>* ‘b000 = ディスプレイのみ<br>* ‘b001 = ディスプレイ Yes/No<br>* ‘b010 = キーボードのみ<br>* ‘b011 = 入力なし、出力なし<br>* ‘b100 = キーボード ディスプレイ                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Block Set Commands in Remote Command Mode | 0x00010000     | このビットをセットした場合、リモートコマンド モードで全ての「Set」コマンドが無効です。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Enable OTA                                | 0x00008000     | このビットをセットした場合、無線 (OTA) による DFUが有効です。それ以外の場合、無線による DFU はサポートされません。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| iOS Mode                                  | 0x00004000     | このビットをセットした場合、接続パラメータが Apple®Bluetooth Accessory Design Guidelines に適合しているかチェックされます。詳細はST,<interval>,<latency>,<timeout>コマンドを参照してください。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Server Only                               | 0x00002000     | このビットをセットした場合、RN4020 モジュールはクライアントとして動作しません。接続の時間と消費電力を節約するため、接続確立後にサービス検出を行いません。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Enable UART in Script                     | 0x00001000     | このビットをセットした場合、スクリプト実行時に通常の UART 出力が許可されます。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Auto-enter MLDP Mode                      | 0x00000800     | このビットをセットした場合、Support MLDP ビットもセットされていると、RN4020 モジュールは接続完了後に自動的に MLDP モードになります。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| MLDP without Status                       | 0x00000400     | このビットをセットした場合、「CMD」、「Connected」、「Connection End」等の追加のステータス文字列はUARTに出力されません。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |

#### サービスのビットパターン

| サービス                         | ビットパターン | Device Information | サービスを使うプロファイル            |
| -------------------------------- | -------------- | ------------------ | ------------------------------------- |
| Device Information               | 0x80000000     | --                 | OTHER SERVICE                         |
| Battery                          | 0x40000000     | --                 | --                                    |
| Heart Rate                       | 0x20000000     | V                  | Heart Rate                            |
| Health Thermometer               | 0x10000000     | V                  | Health Thermometer                    |
| Glucose                          | 0x08000000     | V                  | Glucose                               |
| Blood Pressure                   | 0x04000000     | V                  | Blood Pressure                        |
| Running Speed Cadence            | 0x02000000     | V                  | Running Speed Cadence                 |
| Cycling Speed Cadence            | 0x01000000     | V                  | Cycling Speed Cadence                 |
| Current Time                     | 0x00800000     | --                 | Time                                  |
| Next DST Change                  | 0x00400000     | --                 | Time                                  |
| Reference Time Update            | 0x00200000     | --                 | Time                                  |
| Link Loss                        | 0x00100000     | --                 | Proximity                             |
| Immediate Alert                  | 0x00080000     | --                 | Find Me, Proximity                    |
| TX Power                         | 0x00040000     | --                 | Proximity                             |
| Alert Notification               | 0x00020000     | --                 | Alert Notification                    |
| Phone Alert Status               | 0x00010000     | --                 | Phone Alert Status                    |
| Scan Parameters                  | 0x00004000     | --                 | Scan Parameters                       |
| ユーザ定義のプライベートサービス | 0x00000001     | --                 | ユーザ定義のプライベート プロファイル |


### 機能一覧

* デバイス設定
* デバイス情報サービス
* 工場出荷時の既定値
* アプリケーション タイマ
* ファームウェアアップデート
* UART 制御インターフェイス

* Bluetooth プロファイル (13)
* Bluetooth サービス (17)
  * プライベートサービス
    * MLDP(Microship Low-energy Data Profile)



### サンプル

### BatteryServiceを通信を行う場合

```bash
+
SF,1
SS,40000000
SR,00000000
R,1
A
```

### MLDPモードを使ったRN4020双方向通信を行う場合

MLDPを使用する場合は子機を先に設定し、
親機はFコマンドで子機を探索しそのIDを使いMLDP接続を行う。
"Connected"が表示されたらIコマンドまたはJP2をショートすることでMLDPとなり双方向シリアル通信が可能となる。

#### 子機の設定例

```bash
+
SF,1
SS,32000000
R,1
```

#### 親機の設定例

```bash
+
SF,1
SR,92000000
R,1
F
> xxxxxxxx,0,RNXXXX,XXXXXXXXXXXX,-41
> xxxxxxxx,0,RNXXXX,XXXXXXXXXXXX,-41
> xxxxxxxx,0,RNXXXX,XXXXXXXXXXXX,-41
X
# xxxxxxxxには「F」コマンドで探索したデバイスのIDを設定する。
E,0,xxxxxxxx
```
