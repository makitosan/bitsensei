# micro:bit の Bluetooth LE に関して

## 複数接続

### 使用環境

* Mac OS High Sierra 10.13.4
* Chrome 67.0.3396.79（Official Build） （64 ビット）

### 検証内容

#### 2台

特に問題無く接続可能。コネクションを維持可能な時間の検証はまだ。

#### 6台

Mac OS X の最大接続数は6台らしかったのでその限界で検証する予定。

#### 6台以上

限界を超えての接続可能性を検証する。

## API側で取得可能な情報

### 検証済み

#### 可能なもの

* 加速度センサ
* 地磁気センサ
* 温度
* コンパス

#### 不可能なもの

* 明度（明るさ）センサ
* Web Bluetooth API 使用時
  * [Security and Privacy](https://webbluetoothcg.github.io/web-bluetooth/#security-and-privacy) の項目を参照 [blocklist](https://github.com/WebBluetoothCG/registries/blob/master/gatt_blocklist.txt) でアクセス不可能なUUIDが管理されている。
  * デバイスのSerial Number
    * Device Information Service の Serial Number Characteristics は Web Bluetooth API の仕様として制限されているため取得できない。
    * ただし、接続後の device オブジェクトから id 及び name が取得でき、その id はユニークっぽいので簡易認証には使えるのではないかなぁ・・・

### 未検証

#### 一覧

* 端子（p0-3）
* UART

